---

layout: portfolio-piece
date: 2021-06-28
title: Diet and Nutrition Counter App 
tech: Python, Django, CSS/Bootstrap, HTML
categories: data
contribution: Solo
img-front: ../assets/images/eatright-thumb.jpg
git: https://github.com/peayah/eatrightapp

---

With many diets, it feels like you don't eat enough, don't get enough of a variety to cover your daily needed nutients intake. This app keeps tab on how much you've consumed in a day as well as totalling essetial nutrients. 

The app gives you the ability to add new foods, delete a food if you decided to put that cupcake back :), lists monthly as well as daily consumption plus gives the user the ability to change daily food and nutients targets.

#### What was challenging
Getting the consumption forms to work adding up the nutrients adding the values vs counting the numbers. Adding multiple forms to one page, so that only submitted information from the relevant form is submitted and nothing is submitted twice.


    sum_of_potassium = FoodInstance.objects.filter(consumed__lte=today_end, 
    consumed__gte=today_start).aggregate(Sum('food__potassium')).get('food__potassium__sum', 0.00)

    num_bread = FoodInstance.objects.filter(food__kind__exact='b').filter(consumed__lte=today_end, 
    consumed__gte=today_start).count()
    ...
    
    # Maximum intake intances
    intake_instances = DailyIntake.objects.all()

    # Forms
    bread_form = ConsumeBreadForm(request.POST or None)
   
    ...
   
    if request.method == 'POST':

       elif 'consume_bread' in request.POST:
            if bread_form.is_valid():
                bf=bread_form.save(commit=False)
                bf.save()
                return redirect('index')

