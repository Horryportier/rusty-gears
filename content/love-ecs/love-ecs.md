---
title: Lua + ❤️ + ECS
draft: true
tags: 
  - project
  - lua
  - programming
  - game-dev
---

> *lua-ecs* is my attempt at building [ECS](https://en.wikipedia.org/wiki/Entity_component_system) in [lua](https://lua.org/about.html)  using [Love2d](https://love2d.org/) library. 
> As of now I'm planing on making it good  enough to make some games with it. 


### project repo [love-ecs](https://github.com/Horryportier/love-ecs/)

## Project Overview

The idea for this project was born while playing with [bevy](https://bevyengine.org/).
I was taken away by how easy is to get data that you need.
Ex.
```rust
fn update_position(mut query: Query<(&mut Transform, &Velocity)>) {
  // update position...
}
```
Bevy is great in that regard by creating function with query you are able to
get all valid entities and operate on them. Compering it to [godot](https://godotengine.org/)
where you have to acces "entities" by creating autoload *(global)* scripts 
that menage your them or other rather incontinent ways.
> i'm not good at godot so i might not know the proper way 

I wanted to implement something like that but without caring about all that rust bulishit aka borrow checker. 
Thats why I choose Lua the better language #IndexStartsAt1

## What do we need
- [[World]]
- Entity
- Component
- System
