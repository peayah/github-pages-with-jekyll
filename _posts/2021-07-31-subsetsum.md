---

layout: portfolio-piece
date: 2021-05-31
title: Subset Sum
tech: Python
categories: piece
contribution: Solo
type: (Class Project)

---

Created a function that solve a subset sum problem for any list of integers and a predetermined total. Am able to use to find the optimal combination of integers from a given list to either get close to or hit a total. Could be used to select the optimal combination of packages of different weights to hit a max weight or find a combination of songs that to fill a predetermined runtime.  

#### What was challenging
working out the algorithm and the order in which the different calculstions should happen.

#### What I learned
Although the example was just an array of integers and a target number, I realized the many uses for subset sum set up.


    def main():

    # Integer specific
    # target = 200
    target = 147
    # target = 19
    data_set = [20, 12, 22, 15, 25, 19, 29, 18, 11, 13, 17]

    choices = []
    empty_sublist = Sublist(data_set)
    choices.append(empty_sublist)

    # Loop over data_set
    for number in data_set:

        # Take snapshot of choices
        choice_snapshot = list(choices)

        # Loop over choice_snapshot
        for obj in choice_snapshot:

            # Run add_item with index of current numbers index
            returned_list_obj = obj.add_item(data_set.index(number))

            # Print if sum == target
            if returned_list_obj.sum == target:

                print(returned_list_obj)
                quit()

            # If new sum is smaller than target
            if returned_list_obj.sum < target:

                # Add returned list to choices
                choices.append(returned_list_obj)

        # If no combination equals result, print max
        if data_set.index(number) == data_set.index(data_set[-1]):
            max_obj = max(choices, key=attrgetter('sum'))
            print(max_obj)
            quit()
