# Unity Serialized Dictionary
A serializable Dictionary and property drawer for the Unity Editor, modeled visually after the Odin serialized dictionary.

![alt text](https://github.com/Sterberino/UnitySerializedDictionary/blob/main/Images/Blackboard.png)
### Credits
This project is an extension of [Sterberino's Original Work](https://github.com/Sterberino/UnitySerializedDictionary) and aims to maintain and expand this project as needed for myself and others.
Please also check out [Their GitHub Page](https://github.com/Sterberino) and show them support.

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

## Installation
1. Open up Unity's Package Manager ( **Window > Package Manager** )
2. In the top left, hit the `+`(plus) button and select `Add package from git URL...`
3. In the box, paste the package's git repository, then hit Add

**Repo Link:**

`https://github.com/sim2kid/UnitySerializedDictionary.git?path=Assets/Scripts/Package/UnitySerializedDictionary`
To set a target version, use the release tag like `#1.0.0` at the end of the repo string.

## How To Use
There are two primary scripts you can use to use this package.
The `Blackboard` object allows for a map of `string` to any of the supported values. This can then be accessed as a `Dictionary<string, object>` type.

You can also specify specific Dictionary types if wanted.
To do so, you'll define your dictionary as a type, then define a property drawer in an editor file.

Create a Dictionary Type
```csharp
// TODO: Finish
```

Create a DictionaryDrawer
```csharp
// TODO: Fill In
[CustomPropertyDrawer(typeof(<DRAWER TYPE>))]
public class <NAME>Drawer : DictionaryDrawer<string, <TYPE>> { }
```