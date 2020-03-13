An architecture pattern that allows fast reaction to design changes is one of the most required changes to be implemented.

The main players in the MVVM pattern are:

- The View — that informs the ViewModel about the user’s actions

- The ViewModel — exposes streams of data relevant to the View

- The DataModel — abstracts the data source. The ViewModel works with the DataModel to get and save the data.

<h2> Advantages</h2>
Maintainability
A clean separation of different kinds of code should make it easier to go into one or several of those more granular and focused parts and make changes without worrying.

That means you can remain agile and keep moving out to new releases quickly.

- Testability
With MVVM each piece of code is more granular and if it is implemented right your external and internal dependences are in separate pieces of code from the parts with the core logic that you would like to test.

That makes it a lot easier to write unit tests against a core logic.

Make sure it works right when written and keeps working even when things change in maintenance.

- Extensibility
It sometimes overlaps with maintainability, because of the clean separation boundaries and more granular pieces of code.

You have a better chance of making any of those parts more reusable.

It has also the ability to replace or add new pieces of code that do similar things into the right places in the architecture.

The obvious purpose of MVVM pattern is abstraction of the View which reduces the amount of business logic in code-behind. However, following are some other solid advantages −

The ViewModel is easier to unit test than code-behind or event-driven code.
You can test it without awkward UI automation and interaction.
The presentation layer and the logic is loosely coupled.
<h2>Disadvantages </h2>

-  Some people think that for simple UIs, MVVM can be overkill.
-  Similarly in bigger cases, it can be hard to design the ViewModel.
-  Debugging would be bit difficult when we have complex data bindings
