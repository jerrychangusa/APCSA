author: Jerry Chang
summary: Walkthrough of Dragon Ball Z Game 
id: dragonball-z-game
categories: APCSA
environments: Web
status: Published
feedback link: github.com/changjerry

# Dragon Ball Z Game Project

## Introduction
[Dragon Ball Z] (https://en.wikipedia.org/wiki/Dragon_Ball_Z) is an anime series which features heroes who defend the earth from villains. For this project, you will use your Java skills to build a console game in the spirit of the [Dragon Ball FighterZ game] (https://en.wikipedia.org/wiki/Dragon_Ball_FighterZ).

![caption](dragon-ball-z-fighting.jpg)


## Rules of the Game

Your Dragon Ball Z game is a two-player game where a human player will compete against a computer player in an epic fight! Both players start the game with zero energy points and three life points. The game ends when one player reaches zero life points or after 30 turns.

Every turn, both players must choose one of the following moves:
* Charge Energy (+1 energy point)  🔋
* Attack (-1 energy point)   ⚔️
* Special Attack (-8 energy points) ⚡️
* Defend (0 energy points)          🛡

**Note**: Players can only attack if they have charged up sufficient energy points.

The following table shows the result of a pair of moves chosen by two players:

| **Player 1**       | **Player 2**     |   **Player 1 Result**  | **Player 2 Result** |
| :------------- | :----------: | :----------------: |-----------------: |
|  Charge Energy 🔋 | Charge Energy 🔋| +1 energy point| +1 energy point |
|  Attack ⚔️  | Charge Energy 🔋| -1 energy point | -1 life point, reset energy points|
|  Special Attack  ⚡️ | Charge Energy 🔋| -8 energy point| -3 life points, reset energy points |
|  Defend 🛡  | Charge Energy 🔋| nothing | +1 energy point|
|  Attack ⚔️ | Attack ⚔️| -1 life point, reset energy points| -1 life point, reset energy points |
|  Special Attack  ⚡️  | Attack ⚔️| -8 energy points | -3 life points, reset energy points|
|  Defend 🛡| Attack ⚔️| nothing | -1 energy point |
|  Special Attack  ⚡️  | Special Attack  ⚡️| -1 life point, reset energy points | -1 life point, reset energy points|
|  Defend 🛡 | Special Attack  ⚡️| -3 life points, reset energy points| -8 energy points |
|  Defend 🛡 | Defend 🛡 | nothing | nothing |


## Example Gameplay 

### Begin the Game
When the game starts, the player and computer both start out with 0 energy points and 3 life points.
Print out each player's points to start the game.

```console
Starting the Dragon Ball Z Game!
Player Energy Points: 0
Player Life Points: 3

Computer Energy Points: 0
Computer Life Points: 3
```

### Start a Turn
Prompt the player to select a valid move based on their energy points. If the player does not have
enough energy points for an attack, do not prompt the player to attack.

```console
Turn 1
Select from one of the following moves ("defend", "charge energy"): charge energy
```

### Determine Outcome From Turn 1
Print out the moves that were chosen by the player and the computer as well as the life points and energy points.

```console
Player Move: charge energy
Computer Move: charge energy

Result
Player Energy Points: 1
Player Life Points: 3

Computer Energy Points: 1
Computer Life Points: 3
```

### Start Another Turn
Prompt the player to select a valid move based on their energy points.

```console
Turn 2
Select from one of the following moves ("attack", "defend", "charge energy"): attack
```

### Determine Outcome From Turn 2
Print out the moves that were chosen by the player and the computer as well as the life points and energy points.

```console
Player Move: attack
Computer Move: defend

Result
Player Energy Points: 0
Player Life Points: 3

Computer Energy Points: 1
Computer Life Points: 3
```

### Start Another Turn
Prompt the player to select a valid move based on their energy points.

```console
Turn 3
Select from one of the following moves ("defend", "charge energy"): charge energy
```

### Determine Outcome From Turn 3
Print out the moves that were chosen by the player and the computer as well as the life points and energy points.

```console
Player Move: charge energy
Computer Move: attack

Result
Player Energy Points: 0
Player Life Points: 2

Computer Energy Points: 0
Computer Life Points: 3
```

### End the Game if a Player Loses All Life Points
Prompt the player to select a valid move based on their energy points.

```console
Player Move: charge energy
Computer Move: special attack

Result
Player Energy Points: 0
Player Life Points: 0

Computer Energy Points: 0
Computer Life Points: 1

Computer Wins!
```

### End the Game after 30 turns
Prompt the player to select a valid move based on their energy points.

```console
Player Move: defend
Computer Move: defend

Result
Player Energy Points: 0
Player Life Points: 3

Computer Energy Points: 0
Player Life Points: 3

No winner after 30 turns!
```


## List of Features

