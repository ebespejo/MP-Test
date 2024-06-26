# Battle City

Made by Juan Marco Peralta and Ethan Kurt Espejo for CS 12 MP 1.

## Controls
- The `W`, `A`, `S`, `D` keys are used to move the player tank in an upward, leftward, downward, and rightward direction respectively.
- Press or hold the `SPACEBAR` to fire bullets.
- When the player tank is destroyed, and the player has at least one life remaining, the `F` key is used to respawn the tank.
- When the game is over, the `R` key is used to restart and play again, and the `Q` key is used to quit the program.
- The key sequence of `L`, followed by `O`, and then `L` again serves as a cheat code to give the player an extra life.

### Cells

- **Empty cell**   <img src="https://drive.google.com/uc?id=1HwANx-Ca_FXo1YcTjHZnb58GzEGHKCTX" width="20"><br>
    - Tanks can pass through an empty cell.
- **Brick cell**   <img src="https://drive.google.com/uc?id=1lJDVC5gosy9zg_c9O2Yq-N2LbMsv61qM" width="20"><br>
    - Tanks cannot pass through a brick cell.
    - When hit by a bullet, the brick cell turns into an empty cell, and the bullet disappears.
- **Stone cell**   <img src="https://drive.google.com/uc?id=1p7y4T9NOeYS8M31l0jB0ov36CBUosb3o" width="20"><br>
    - Tanks cannot pass through a stone cell.
    - When hit by a bullet, the stone cell remains a stone cell, and the bullet disappears.
- **Mirror cell**   <img src="https://drive.google.com/uc?id=1OAmHQ6OtWTlGuFbOWZzkU6HzHE7zen5K" width="20"><br>
    - Tanks cannot pass through a mirror cell.
    - There are two *orientations:* northeast-leaning and southeast-leaning.
    - When hit by a bullet, the bullet bounces depending on the orientation.
    - The following image illustrates mirror cells. The top four illustrate bullet-bouncing mechanics for northeast-leaning mirror cells; the bottom four for southeast-leaning mirror cells.
<br><img src="https://drive.google.com/uc?id=1b0Ob8u_cHqYv_aEoG9FuSdiGKCkOE129" width="500"><br>
- **Water cell**   <img src="https://drive.google.com/uc?id=1ASMCymvprOOPLpb7duYt9QqUIOX-FwRy" width="20"><br>
    - Tanks cannot pass through a water cell.
    - Bullets pass through water cells.
- **Cracked brick cell**   <img src="https://drive.google.com/uc?id=1sTiAah1itP0iD7m2LFakTzye4B1cHDuo" width="20"><br>
    - This represents a “partially broken” version of a brick cell.
    - Tanks cannot pass through a cracked brick cell.
    - When hit by a bullet, the cracked brick cell turns into an empty cell, and the bullet disappears.
    - If cracked brick cells are implemented, a bullet hitting a brick cell turns it into a cracked brick cell (instead of an empty cell).
- **Forest cell**   <img src="https://drive.google.com/uc?id=1YkOK0vG8Z2ho_Bq2p1qMa2D32w_ycqqf" width="20"><br>
    - Tanks can pass through a forest cell.
    - Forest cells act pretty much like empty cells, except they *partially obscure* tanks passing through them.
- **Home cell**   <img src="https://drive.google.com/uc?id=1CMWhakLnl_yx6G0f_Ldn8Nw0Vk260_x_" width="20"><br>
    - Tanks cannot pass through a home cell.
    - When a bullet hits a home cell, it is destroyed, and the game is instantly over (regardless of the number of lives of the player).

### Tanks
- **Player Tank**   <img src="https://drive.google.com/uc?id=1aRPilh-FcQww5K-TTchzN0ZvTorgKWyf" width="20"><br>
    - Controlled by player using the `W`, `A`, `S`, `D` keys.
- **Enemy Tank**   <img src="https://drive.google.com/uc?id=1xjvMUjM-Fc2s6YaDcm5q3m2uB3tJra9q" width="20"><br>
    - Requires 1 hit to destroy.
 - **Boss Enemy Tank**   <img src="https://drive.google.com/uc?id=162WMqmk_YpH1wbVSE590JOCOMwb4o5a4" width="20"><img src="https://drive.google.com/uc?id=1IcbwcLhB6HBwy0do15YrfAe5KpY1rv6h" width="20"><img src="https://drive.google.com/uc?id=1wgZioFfNu_bpN2anCcoudhD3fhfPRgpp" width="20"><br>
    - The hits needed to kill a boss tank is randomized from 1-3 hits.

### Power-ups
- **Faster Speed**   <img src="https://drive.google.com/uc?id=14dO_V2aTfZ4pYbrCyhDy7za5DNrjZSzC" width="20"><br>
    - Doubles the player's speed.
- **Extra Life**   <img src="https://drive.google.com/uc?id=1dCW0FWeP_DnSHEiueNxHn5P-P1aTKpfF" width="20"><br>
    - Gives the player an extra life.


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

<br><br>
**Stage 1 should look like this:**<br>
<img src="https://drive.google.com/uc?id=1skzxchx3kPagxhbEjlkAotcpMDRlgZpF" width="500"><br>
_Note that the enemy tanks in the picture have not completely spawned yet._
<br><br>

**Stage 2 should look like this:**<br>
<img src="https://drive.google.com/uc?id=1ZATuDnf6S3Xs5gN66wzxBsJFdre4KWOZ" width="500"><br>
_Note that the enemy tanks in the picture have not completely spawned yet._
<br><br>
## Phase
The highest phase we were able to accomplish is **Phase 3**.

## Contributions
**Juan Marco Peralta**
- Main game program
- Testing

**Ethan Kurt Espejo**
- Game design (tanks, blocks, sounds)
- Testing

## Video Demo
[https://drive.google.com/drive/folders/1_-XWOK_jRqmUqBkcnhxVPyhYdK0TMoX7?usp=sharing](https://drive.google.com/drive/folders/1_-XWOK_jRqmUqBkcnhxVPyhYdK0TMoX7?usp=sharing)
