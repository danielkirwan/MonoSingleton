This is a generic use case singleton class for use in Unity

To use it -> Copy the code into your project -> Then Inherit from MonoSingleton"<yourclassname>" and you will now have a class that will be a singleton with Mono behaviours.

You can disable the dontdestroyonload method by using the bool _wantToDestroyOnLoad. 
Either handle this in code on your class or by using the serialized field in the Unity editor.

Good luck and enjoy
