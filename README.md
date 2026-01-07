# MonoSingleton

![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![Pattern](https://img.shields.io/badge/Pattern-Singleton-blue?style=for-the-badge)
![Runtime](https://img.shields.io/badge/Runtime-MonoBehaviour-orange?style=for-the-badge)

A lightweight **generic MonoBehaviour singleton base class** for Unity, designed to reduce boilerplate and provide a consistent, reusable pattern for global runtime systems.

---

## ✨ Features

- Generic `MonoSingleton<T>` base class
- Works with **MonoBehaviour-based** systems
- Optional `DontDestroyOnLoad` behaviour
- Lazy-accessible static `Instance`
- Prevents duplicate instances at runtime
- Simple, extensible, and production-friendly

---

## 📄 Overview

`MonoSingleton<T>` is intended for **global game systems** such as:

- Audio managers  
- Game state managers  
- Save systems  
- Analytics / telemetry  
- Service-style runtime managers  

It avoids manual instance wiring while still allowing scene-based setup.

---

## 📦 Installation

1. Copy `MonoSingleton.cs` into your Unity project  
   (e.g. `Assets/Scripts/Core/Patterns/`)
2. Place it in a namespace of your choice (default: `DangryGames`)
3. Inherit from `MonoSingleton<T>` instead of `MonoBehaviour`

---

## 🧩 Usage

### Basic example

```csharp
using UnityEngine;
using DangryGames;

public class AudioManager : MonoSingleton<AudioManager>
{
    protected override void Awake()
    {
        base.Awake();
        // Custom initialisation
    }

    public void PlaySound()
    {
        Debug.Log("Playing sound");
    }
}
