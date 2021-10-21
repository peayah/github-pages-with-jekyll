---

layout: portfolio-piece
date: 2021-05-31
title: Binary Search Tree Deletion
tech: Python
categories: piece
contribution: Solo
type: (Class Project)
published: True

---

Code that lazy-deletes and hard deletes nodes in Binary Search Tree. Traverses tree and when searching for particular node, is able to differentiate between not deleted, lazy-deleted and hard deleted nodes. 

#### What was challenging
understanding and working around nodes deleted in the middle of a tree and still be able to find nodes after the deleted node.

#### What I learned
Working in and travering trees is quite the brain workout. Working with lazy delete vs hard delete (garbage collection) where with the first I just had to work around it but with the latter I had to connect the before and after of the deleted node.

    # revise remove(0 to implement lazy deletion
    def remove(self, data):

        self._root = self._remove(data, self._root)

    def _remove(self, data, sub_root):

        if sub_root is None:
            raise LazySearchTree.NotFoundError

        if data < sub_root.data:
            sub_root.left_child = self._remove(data, sub_root.left_child)

        elif data > sub_root.data:
            sub_root.right_child = self._remove(data, sub_root.right_child)

        if data == sub_root.data:
            if sub_root.deleted is True:
                raise LazySearchTree.NotFoundError
            sub_root.deleted = True
            self._size -= 1

        return sub_root

    # add a public/private pair collect_garbage
    def collect_garbage(self):
        self._root = self._collect_garbage(self._remove_hard, self._root)

    def _collect_garbage(self, function, sub_root):

        if sub_root is None:
            return

        if sub_root.left_child is not None:
            self._collect_garbage(function, sub_root.left_child)

        if sub_root.right_child is not None:
            self._collect_garbage(function, sub_root.right_child)

        if sub_root.deleted is True:

            data = sub_root.data

            sub_root = function(data, self._root)

        return sub_root

    # Takes only what  comes from collect_garbage
    def _remove_hard(self, data, sub_root):

        if sub_root is None:
            raise LazySearchTree.NotFoundError

        if data < sub_root.data:
            sub_root.left_child = self._remove_hard(data, sub_root.left_child)

        elif sub_root.data < data:
            sub_root.right_child = self._remove_hard(data, sub_root.right_child)

        elif sub_root.left_child is not None and sub_root.right_child is not None:
            sub_root.data = self._find_min(sub_root.right_child)
            sub_root.right_child = self._remove_hard(sub_root.data, sub_root.right_child)
            sub_root.deleted = False

        else:
            sub_root = sub_root.left_child if sub_root.left_child is not None \
                else sub_root.right_child

            self._hard_size -= 1

        return sub_root

    
