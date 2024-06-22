# Battle City

Made by Juan Marco Peralta and Ethan Kurt Espejo for CS 12 MP 1.

## Controls
- The `W`, `A,` `S`, `D` keys are used to move the player tank in an upward, leftward, downward, and rightward direction respectively.
- Press or hold the `SPACE BAR` to fire bullets.
- When the player tank is destroyed, and the player has at least one life remaining, the `F` key is used to respawn the tank.
- When the game is over, the `R` key is used to restart and play again, and the `Q` key is used to quit the program.
- The key sequence of `L`, followed by `O`, and then `L` again serves as a cheat code to give the player an extra life.

## Instructions

Before playing the game, make sure that there is a stage file `Stages.py` in the same folder as `BattleCity.py`.

### Stage File

The stage file is a Python program file that should have a list of lists named `STAGES`, containing the lists of strings representing the map of each stage.

The dimensions for each map must be **13x13**.

**Example of a stage file:**
```python
STAGE_1 = [
    "E000000000S0E",
    "SBBBFF000B000",
    "E0000BBBBB0BB",
    "000000000000O",
    "00000BBBBBB00",
    "00M000000ES00",
    "000S0WWWFFF00",
    "000B000000000",
    "SBFB0E000000F",
    "0B0B0BBB000B0",
    "0B0W00P0000B0",
    "0B0S0BBB000B0",
    "0BES0BHB00BBE"
]

STAGE_2 = [
    "M00000000000E",
    "00FF000000F00",
    "0FBBF0000FBF0",
    "00FFEWF0FBFE0",
    "00000FBF0F000",
    "F00000F000000",
    "BF000FE00F000",
    "SBFWFBFWFBF00",
    "BF000F00FBF00",
    "F00000000F000",
    "000000F00000E",
    "00F00FBF000BB",
    "EFSF0FSF00PBH"
]

STAGES = [STAGE_1, STAGE_2]
```

The legend for creating a map is as follows:
- `P`: Player tank's starting position
- `E`: Enemy spawn point
- `S`: Stone cell
- `B`: Brick cell
- `C`: Cracked brick cell
- `W`: Water cell
- `F`: Forest cell
- `H`: Home cell
- `M`: Northeast-leaning mirror
- `O`: Southeast-leaning mirror

Stage 1 should look like this:
<img src="https://drive.google.com/uc?id=1skzxchx3kPagxhbEjlkAotcpMDRlgZpF" width="500"><br>
_Note that the enemy tanks in the picture have not completely spawned yet._

Stage 2 should look like this:
<img src="https://drive.google.com/uc?id=1ZATuDnf6S3Xs5gN66wzxBsJFdre4KWOZ" width="500"><br>
_Note that the enemy tanks in the picture have not completely spawned yet._

## Phase
The highest phase we were able to accomplish is **Phase 3**.

## Contributions
**Juan Marco Peralta**
- Main game program

**Ethan Kurt Espejo**
- Game design (tanks, blocks, sounds)

## Video Demo
<drive link>
