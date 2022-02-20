## How to implement Interface?

In our game, we are using the interface for the damage system. For this, first, we have to create an interface called IDamagable. But remember if you are making an interface, always the name of that interface will start with I then followed by any name like - IShootable, IPickable, etc.

Like this -
```C#
public interface IDamagable
    {
        void TakeDamage(float damage);
    }
```
Now we have created an interface, let’s see how to use it. In order to use it, you have to inherit the interface first and then implement all the methods which are inside it. 

Like this -
```C#
public class EnemyView: Monobehaviour, IDamagable
	 {
				public void TakeDamage(float damage)
        {
            controller.ApplyDamage(damage);
        }
	 }
```
EnemyController -
```C#
public class EnemyController
	 {
				public void ApplyDamage(float damage)
        {
            if (model.health <= 0) return;

            if (model.health - damage <= 0)
            {
                //enemy dead
            }
            else
                model.health -= damage;
        }
	 }
```
Like this, you can use it for damaging the player tank also.

---
## Repository of Battle Tank game
In order to test your skills, Checkout the repository below for,

Problem Statement and Solution for the Damage System of Battle tank game.

https://github.com/outscal/Battle-Tank-Damage-System-Project
