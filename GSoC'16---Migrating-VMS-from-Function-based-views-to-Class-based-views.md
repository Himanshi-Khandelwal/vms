Systers’ Volunteer Management System currently uses function based views. It repeats certain patterns again and again, and is mostly redundant. Function based views are deprecated after python version 1.3. Class Based generic views helps to streamline common use cases, saving development time and effort.
One of the advantages of CBV is Inheritance. For instance, large projects like VMS has a lot of redundant code due the repetition of similar views. By migrating to CBV, views could be inherited and thus avoid code redundancy.

Few advantages, which VMS can achieve by migrating to Django’s class based views are :

Django offers various generic views like CreateView, UpdateView, FormView, ListView and DetailView to handle views easily. For eg: Allow users to Create, Update and Delete events and shifts of volunteers with or without authorization, without violating DRY.
Better code readability, reducing the number of lines of code, easing the code review process.
Replacing the decorators by mixins instead, makes them more flexible, extensible and DRYer, just like the move from FBVs to CBVs.
Better handling of form data, which is handled in a traditional way in FBVs.
Better support from the Django development community as the recent developments are CBV based.
Considering various advantages of shifting to CBV, I propose this migration for all the apps in VMS to be a Google Summer of Code 2016 project, and I have come up with a proposal for the same. The following are the tasks to be completed for migration of VMS to CBV

### Completed Tasks
* Migrating home app to CBV
* Migrating authentication app to CBV
* Migrating administrator app to CBV
* Migrating event app to CBV
* Migrating job app to CBV
* Migrating registration app to CBV
* Migrating volunteer app to CBV
* Migrating shift app to CBV
* Migrating organization app to CBV