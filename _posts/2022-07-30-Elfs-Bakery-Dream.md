---
layout: post
title: Project:Elf's Bakery Dream - Behind the Game
categories: [Projects]
tags: [Projects, Game Design, Functional Programming, Elm]
date: '2022-07-30 16:42:38 -0600'
img_path: /assets/img/post/
---

> The source code of the game together with other presenting materials could be found at the GitHub repo [Elfs-Bakery](https://github.com/ziming-zh/Elfs-Bakery/)
{: .prompt-info }

> Click [here](https://focs.ji.sjtu.edu.cn/silverfocs/demo/2022/p2team17/) to play our game. Since arrow keys are required for character manipulation, please play our games on computers for better game experience.
{: .prompt-tip }

## Introduction 

Our designed game "Elf's Bakery" is a project of UM-SJTU JI 2021-2022 Summer course VG100-3, using Elm to implement a web game Elf's Bakery designed by the team Miu Gamers. The game is fully implemented using functional programming language *Elm*. revolves around helping a little Elf pursue its Bakery Dream by engaging in various activities within the game. Players are tasked with manipulating the Elf using arrow keys, pushing valves, creating proper routes, bringing magic creams to their destination, and making correct cakes. As players progress, they become more senior bakers and work towards realizing the Bakery Dream.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-1.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Game poster of Elf's Bakery </div>
</center>

## Game Elements 

In "Elf's Bakery," players encounter various game elements that contribute to the overall gameplay experience. These elements include valves, magic creams, toppings, and exits. By understanding and interacting with these components, players can progress through the game and help the little Elf achieve its Bakery Dream.



### Valves

Valves play a crucial role in the game, allowing players to control the path of the magic creams. By strategically rotating the valves, players can open paths in different directions, thereby influencing the movement of the magic creams within the game environment. This mechanic adds a layer of puzzle-solving and strategic thinking to the gameplay, as players must plan their valve manipulations to guide the creams effectively.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-2.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Basic game elements of Elf's Bakery </div>
</center>

### Magic Creams

The magic creams within the game exhibit unique behavior, as they are designed to follow the shortest viable path towards the exit. The creams are differentiated by color, with deeper colors indicating longer distances. This characteristic adds a dynamic element to the gameplay, as players must consider the movement and merging of creams to achieve the desired outcomes in cake creation.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-4.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Color merging and cake builidng principles </div>
</center>

### Toppings

Furthermore, the introduction of toppings presents an additional challenge for players. Picky customers within the game may demand specific toppings, such as vanilla and chocolate, to be added to particular layers of the cake. To fulfill these demands, players must guide the relevant cream across the toppings, ensuring that they are incorporated into the cake-making process and ultimately reach the exit. This mechanic adds a layer of precision and attention to detail, as players must carefully manage the flow of creams to satisfy customer requirements.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-3.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Cake colors and toppings </div>
</center>

## Game Levels

As players navigate through the game's levels, they encounter increasingly complex challenges related to cake-making. The game's progression introduces multi-layered cakes with various decorations, requiring players to employ additional techniques to successfully complete each level. This escalation in complexity ensures that players are continually engaged and challenged as they advance through the game, providing a sense of accomplishment as they master new cake-making techniques and overcome more intricate obstacles.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-8.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Elf's Mission </div>
</center>

In summary, "Elf's Bakery" offers players an engaging experience as they assist the Elf in navigating through challenges, creating delicious cakes, and ultimately realizing the Bakery Dream. It is a freshman team projects for a three-member team, and a lot of the places, for example, the smoothness of the animation and the quality of the footages, could be further improved. We holpe that in general the game's cohesive level design, original game mechanism, and lovely interface contribute to an immersive and enjoyable gaming experience





## Game Snapshots

### Easy Level

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-5.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Level 2-3: Junior Pastry Chef </div>
</center>

### Medium Level

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-6.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Level 4-6: Senior Pastry Chef </div>
</center>

### Hard Level

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ELF-7.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Level 7: Custeau Chef </div>
</center>

### Contributors

UM-SJTU JI SU22 ENGR1000J-3 p2team-17

- Ziming Zhou 521370910142

- Chongye Yang 521370910088

- Qijia Liu 521370910165
