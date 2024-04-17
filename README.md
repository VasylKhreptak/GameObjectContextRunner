Problem: When using FishNet or any other networking plugin, objects are created via the Instantiate() method. Therefore the dependencies are not injected. 
Possible solution: you can add ZenAutoInject, but this solution does not work when using this component with the "Search in Hierarchy" option (Nullreference Exception).
My solution: this script runs at the beginning (before Awake()) of the object creation and calls the GameObjectContext constructor. All dependencies are injected successfully.
