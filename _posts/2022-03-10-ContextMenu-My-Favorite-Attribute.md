---
title: ContextMenu My Favorite Attribute
date: 2022-03-10
categories: [Gamedev, Unity]
tags: [tips]
---

## ContextMenu, My Favorite Attribute

Today I would like to talk about Unity's attribute ContextMenu: [ContextMenu](https://docs.unity3d.com/ScriptReference/ContextMenu.html)

It allows to add commands to the context menu on Editor, just add before a function without parameters (private or public), right-click the script component, and BOOM, there is a new item menu that executes whatever your function does. It works both on Editor and Play Mode.

Example:
```
using UnityEngine;

public class ContextTesting : MonoBehaviour
{
    /// Add a context menu named "Do Something" in the inspector
    /// of the attached script.
    [ContextMenu("Do Something")]
    void DoSomething()
    {
        Debug.Log("Perform operation");
    }
}

```

I really like to use it to both automate setups in the scene and test function in play mode, without the hassle to add "Input.OnKeyDown(...){DoTheThing()}". Also it's pretty safe to leave it on the code, since it doesn't affect the final compiled game. Also, it's pretty fast to implement, the other alternative being creating a custom Editor script and adding an Editor button.

This is my tip of the day.

Till Next Time!


