# Game-Dev-Tool-Kits | Guided Projectile

## Overview
`GuidedProjectile` is a **flexible Unity C# base class** for creating projectiles with various guidance systems in both **2D** and **3D**.  
It’s designed for **reusability and extension**, making it suitable for homing missiles, magic spells, or AI-controlled weapons.

## ✨ Key Features
- **2D & 3D Support** – works with both `Rigidbody2D` and `Rigidbody`.
- **Guidance Modes**:
	- **Guided** – Tracks a moving or static target in real-time.
	- **Controlled** – Moves based on player input (e.g., joystick).
	- **Unguided** – Moves in a straight path based on initial direction.
	- **Predictive** – Estimates and intercepts a moving target’s future position.
- **Customizable Movement**:
	- Adjustable `projectileSpeed` and `projectileTurnSpeed` for fine-tuned control.
- **Flexible Targeting**:
	- Supports both `Transform` targets and `Vector3` positional targeting.
- **Extendable Input Logic**:
	- Override `ProjectileInput` for custom input handling in controlled mode.

## 🛠 Usage

### 1. Inherit the Class
```csharp
	public class MyClass : GuidedProjectile {
		... Your Code
	}
```

### 2. Implement in FixedUpdate
```csharp
	void FixedUpdate () {
		ProjectileInput(InputVector); // Only if in Controlled mode
		ProjectileGuidanceDirection();
	}
```

## 📦 Dependencies
This script references my **private utility libraries**:
- `CustomAttributes` (editor attributes like `[ReadOnly]`, `[LineDivider]`, etc.)
- `GameMechanicUtility` (helper functions)

> These utilities are only used for editor polish (e.g., attributes like [ReadOnly]) 
> and convenience functions. They are not required to understand or evaluate 
> the core projectile logic shown here.


## ⚠️ Disclaimer
This script is provided as a **code sample** only.  
It is meant to showcase my coding style, architecture, and approach to reusable gameplay systems.