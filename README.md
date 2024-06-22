## Controls
- The `W`, `A,` `S`, `D` keys are used to move the player tank in an upward, leftward, downward, and rightward direction respectively.
- Press or hold the `SPACEBAR` to fire bullets.
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

![Example Image](https://drive.google.com/uc?id=1skzxchx3kPagxhbEjlkAotcpMDRlgZpF)

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

