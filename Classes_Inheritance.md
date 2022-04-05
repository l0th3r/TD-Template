# Classes Chart

Those diagrams explain classes organisation and inheritance in the Tower Defense Template.\
[Help to understand diagrams ?](https://mermaid-js.github.io/mermaid/#/classDiagram)

> **_Warning:_**  This document is not complete.

## TD_Entity
```mermaid
 classDiagram
      TD_Entity <|-- TD_Entity_Movable
      TD_Entity <|-- TD_Building
      TD_Entity <|-- TD_Weapon
      
      TD_Building <|-- TD_Tower
 
      class TD_Entity
        TD_Entity: Implement mesh, health and damage system.
      
      class TD_Entity_Movable
        TD_Entity_Movable: Add grid based movements over the grid.
        
      class TD_Weapon
        TD_Weapon: Add the use of projectile and targetting on grid.
        
      class TD_Building
        TD_Building: Add Static entity with link with a grid platform.
      
      class TD_Tower
        TD_Tower: Add a link to a weapon.
```

## TD_Platform
```mermaid
 classDiagram
   TD_Platform  <|-- TD_Platform_Building
   TD_Platform  <|-- TD_Platform_Path
   TD_Platform  <|-- TD_Platform_Empty
   TD_Platform_Building <|-- TD_Platform_Building_Interactible
 
   class TD_Platform
     TD_Platform: Used in a grid, allow to materialize the grid.
     
   class TD_Platform_Building
     TD_Platform_Building: A platform that can statically hold a TD_Building entity.
     
   class TD_Platform_Building_Interactible
     TD_Platform_Building_Interactible: Allow player interaction.
     TD_Platform_Building_Interactible: Allow the player to dynamically change the building.
   
   class TD_Platform_Path
     TD_Platform_Path: Used to generate paths and in pathfinding.
     
   class TD_Platform_Empty
     TD_Platform_Empty: A platform with no mesh.
```

## Others
```mermaid
 classDiagram
      class TD_Projectile
        TD_Projectile: Actor meant to inflict damages to an entity on contact.
```
