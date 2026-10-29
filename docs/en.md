# Cthangover: Starter Party — who the player begins with

This small mod gives a new game of Cthangover its starting state: Marao in the party and the skill Slave Trader in the skill collection. It holds only this code; the character and the skill themselves are data of the base game and of the skills engine.

## What a new player has

The character panel at the very start of Cthangover — one party member, Marao, with two actions and a free slot:

![The Character actions panel: Party 1, Marao (template 2, HP 16/16, AP 1, ATK 5, DEF 0) with Basic attack and Defence, and an empty third slot.](assets/party.jpg)

The skills panel — one skill, Slave Trader:

![The Skills panel: the collection holds one Epic passive skill, Slave Trader, "+10% recruitment chance", with the description "Gives the ability to enslave a defeated enemy with a base chance of 10%. The upkeep of the slave falls on your shoulders." and the collection effect +10% recruitment chance.](assets/skills.jpg)

Slave Trader is what lets the player capture defeated enemies (see Recruiting): without it no enemy can join.

## When it runs

- When the game's mods are ready, the mod adds the character `Marao` to the party and grants the skill `slave_master`.
- Every time a **new game** starts it does the same again, because a new game first clears the party.
- Loading a save replaces the party and skills with the saved ones. Both steps can run more than once safely: Marao is not added twice and the skill is not granted twice.

## Changing the start

- Another mod can add more starting characters the same way: a C# initializer that adds its characters to the party when the mods are ready.
- To start without Marao or without the skill, leave this mod out of the game's collection and seed the party in your own mod.

## Known problems

- The Slave Trader card has no picture: the skill's image is missing.
- The card and its description promise "+10% recruitment chance", but no code reads that bonus; the capture roll uses only the enemy's own chance.
