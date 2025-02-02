# Unity Serialized Dictionary
A serializable Dictionary and property drawer for the Unity Editor, modeled visually after the Odin serialized dictionary.

![alt text](https://github.com/Sterberino/UnitySerializedDictionary/blob/main/Images/Blackboard.png)
### Credits
This project is an extension of [Sterberino's Original Work](https://github.com/Sterberino/UnitySerializedDictionary) and aims to maintain and expand this project as needed for myself and others.
Please also check out [Their GitHub Page](https://github.com/Sterberino) and show them support.

**This Repo is no longer maintained.**
The project has been moved to [sim2kid/UnitySerializedDictionary](https://github.com/sim2kid/UnitySerializedDictionary). Please use that repo for package updates and issues.

## How It Works

It uses `ISerializationCallbackReceiver` to convert keys and values to serializable lists in the background, to allow for dictionary serialization in the editor. 
Mostly uses switch statements to identify the type and handle drawing the editor fields and serializing/de-serializing values. 
It allows for dynamically changing dictionary value types at runtime, and it supports:
  - [UnityEngine.Object](https://docs.unity3d.com/ScriptReference/Object.html) (asset references and in scene components/ GameObjects)
  - all the basic Number types, strings, and bool
  - enums of any type
  - All [Vector](https://docs.unity3d.com/Manual/VectorCookbook.html) types
  - [Bounds](https://docs.unity3d.com/ScriptReference/Bounds.html) / [BoundsInt](https://docs.unity3d.com/ScriptReference/BoundsInt.html) and [Rect](https://docs.unity3d.com/ScriptReference/Rect.html) / [RectInt](https://docs.unity3d.com/ScriptReference/RectInt.html)
  - [Gradients](https://docs.unity3d.com/ScriptReference/Gradient.html), [Animation Curves](https://docs.unity3d.com/ScriptReference/AnimationCurve.html), and [Color](https://docs.unity3d.com/ScriptReference/Color.html)
  - Any struct or class that is serializable using [JsonUtility](https://docs.unity3d.com/ScriptReference/JsonUtility.html) (Although there is no general drawer for it yet)
