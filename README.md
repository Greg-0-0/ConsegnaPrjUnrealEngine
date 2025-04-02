# ConsegnaPrjUnrealEngine
Turn-based Strategic Game

Index:
1. Game features
2. Rules 
3. End game
4. Menu
5. User Interface

1. The game is played between two players: a human player and an Ai player. Each player has two units: a brawler with a maximum movement of 6 tiles in every direction, an attack range of 1 tile in every direction, a point life of 40 and an attack damage range [1;6]. Then there is the sniper with a maximum movement of 3 tiles in every direction, an attack range of
10 tile in every direction, a point life of 20 and an attack damage range [4;8]. There is also a mechanism of counterattack that works this way: every time a sniper attacks the enemy sniper or the enemy brawler, while being in the attack range of the brawler, a damage by counterattack is applied to the offensive unit. The damage of the counterattack ranges from 1 to 3. The game is played on a field with obstacles, these elements occupie the tiles, making them unusable by units.

2. The players take turns alternatively sarting randomly with one of them. 
There are two game phases:
- Placing phase: units are placed on tiles by clicking on them. Units cannot be placed on a tile occupied by another unit or an obstacle.
- Attacking/Moving phase: after selecting a unit by clicking on it, it can be moved on the tiles inside the range of movement (green colored). The unit can also attack an enemy unit, if it is in range, in this case the tile of the opponent unit is red colored. The attack can be carried out before or after the movement, however, if done before moving the unit, the unit cannot move anymore. In any case during a turn both units have to move or attack to consider the game valid.

3. A match can terminate under three circumnstances:
- A win/lose situation: both units' health of a player reach 0, at this point the game ends with a screen message displaying the winning player, then the game resets automatically to start a new match.
- A tie: since there is a counterattack mechanism, the game could end in a tie, if both last units die by the same attack, even in this case an appropriate message is displayed on the screen and then the match resets automatically.
- Deadlock: it can happen that a unit cannot move nor attack, even after moving the other unit, which could help unlock the situation, in this case an appropriate message is displayed on the screen and then the match resets automatically.

4. Before the game starts a menu shows, here two settings can be chosen before starting the game;
- Obstacle percentage: from a minimum of 0 (no obstacle) to a maximum of 99, 100 isn't selectable, since this results in no free tiles, preventing the game from starting, .
- Ai level: Ai can be Random or Smart, meaning a Random Ai will move and attack based on random decisions, while a Smart Ai will attack whenever possible and move towards enemy units to enter attack range.

5. The User Interface displays different information:
- In the top-left-corner the turn of who is placing/attacking/moving is displayed.
- In the top-right-corner there is a section to show the matches won by the Ai (Random or Smart), by the human and the total matches played. These values refers to only one game session started after clicking the Play button in the menu. When going back to the menu the values are set to zero. This happens since, when going back to the menu, the Ai level could change, thus changing the competitiveness of the Ai.
- On the left side it's displayed the history of every move, including: placing a unit on a tile, moving a unit from a tile to another tile and attacking a unit with relative damage dealt.
- On the right-middle side the status of both unit of both players is shown, a label "Dead" will be added once the unit reaches 0 health.
- On the bottom-right-corner three buttons are displayed.
The first one is an EndTurn button that allows to end a turn after moving a unit, in case the player doesn't want to attack. It is displayed only when clickable. The second one si the Reset button which will reset the game, note that this action won't influence the score of any player or the total matches played. The third one is the ChangeSettings button, which allows to go back to the menu and change settings, this results in a reset of the game field and the scores/matches played.
