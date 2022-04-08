# VoltorbFlip
A WPF game I made in Grade 12 based on the popular Pokemon minigame.
Unfortunately I've lost the source code for this project, but I can try my best to explain how it works.

![main menu](/screenshots/menu.png)

## How it works
### Save States
One of the features of this game is the save states. While playing the game, the player will earn coins each round. Their total coins score is saved every time it updates to the [save file](/Resources/SaveFiles.txt). In practice, this is just a txt file that saves a single number for each save indicating total coins, where each row in the file represents a different "save file". I have kept a couple of my save files in the repos [save file document](/Resources/SaveFiles.txt) to give an example.
### Gameplay
When the user starts the game, it opens a new window with the game board. Each tile is simply a button element with a png as its background. In fact, the reason why you can't play this game in fullscreen is because the buttons change size based on the window size, which would ruin the look of the tiles. When the player clicks a tile button a method is run that "selects" the tile and changes the button's background to add a red cursor.

![gameplay](/screenshots/mid-game.png)

Once a tile is selected, the player has a few options: they can click the flip button on the right to reveal what was on the selected tile or they can choose one of the various marker buttons on the left to mark the tile with possible tile contents. Clicking a marker button will update the background of the selected tile's button to mark the tile. If the player flips the tile, another method is run to check if the currently selected tile has a bomb. If it does, the player loses their current coins and the board contents are revealed. If the tile does not have a bomb, the number value of the tile is revealed, and the player is awarded the respective amount of coins. (I can't remember exactly how coins were awarded, but I think a 2 or 3 gives the player 2 or 3 coins, whereas a 1 awards nothing.)

If the player flips over every tile with a value over 1, the player wins and their coins are added to their total. The board is also revealed to show the position of the bombs. If the player clicks "new game", a new round will start with an extra bomb added to the board. (There is also a limit to the number of bombs but I forget what it is.) If the player decides mid-game to stop playing, they also have the option to "cash in" which ends the round and saves their current coins to their total. This is useful in the event where the player does not have enough information and must guess between two tiles to win the game.

![game win](/screenshots/game_win.png)

## How to play
I will write this section soon, but unfortunately I have schoolwork that needs to be completed first.

If you want to play the game, just make sure you download the [App](Voltorb_Flip.exe) and [Resources folder](/Resources) to the same directory.
