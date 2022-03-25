# Classes Chart

This diagram explain classes organisation and inheritance in the Tower Defense Template.\
[Help to understand this diagram ?](https://mermaid-js.github.io/mermaid/#/classDiagram)

> **_Warning:_**  This document is not complete.

```mermaid
 classDiagram
      TD_Entity <|-- TD_Entity_Movable : Inherit
 
      class TD_Entity
        TD_Entity: Implement a model, health and damage system
        TD_Entity: -
        TD_Entity: int MaxHealth
        TD_Entity: bool UsesHealth
        TD_Entity: bool CanBeDamaged
        TD_Entity: AddHealth()
      
      class TD_Entity_Movable
        TD_Entity_Movable: Add grid based movements over the grid
        TD_Entity_Movable: -
        TD_Entity_Movable: float MoveSpeed
        TD_Entity_Movable: float AttackCoolDown
        TD_Entity_Movable: int AttackDamages
        TD_Entity_Movable: StartGridMovements()
```
