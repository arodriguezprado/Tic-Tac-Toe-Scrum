# Tic Tac Toe - Scenarios BDD

## Feature:  Tic Tac Toe game

### Scenario: Player chooses which piece wants to use
- **Given**  The game asks which piece the Player would like to use if X or O
- **When** Player chooses X
- **Then** The other player or the boot gets the piece O by defult


### Scenario: Player chooses which piece wants to use
- **Given**  The game asks which piece the Player would like to use if X or O
- **When** Player chooses O
- **Then** The other player or the boot gets the piece X by default


### Scenario: Player X makes a move
- **Given** empty dashboard
- **When**   The player X moves the first piece
- **Then** the dashboar shows the piece X on the positon it was placed

---
### Scenario: Locked positions on the dashboard
- **Given** Player X made a move
- **When** Player X made a move, the position where the piece was placed gets locked 
- **Then** The dashboard doesn't let player O place the piece on the same spot

---
### Scenario: Player chooses a locked position
- **Given**  The player chooses a locked position
- **When** The position choosed is locked so the game shows a message "This position is alredy used"
- **Then** The game asks the player to choose an empty position

### Scenario: Player O makes a move
- **Given** Player X placed the first piece 
- **When** Player O has to make a move  
- **Then** Player O makes a move to an empty position on the dashboard
---

### Scenario: Player X wins a line 
- **Given** Player X took the positions 1,2 and 3  
- **When** Player X has a full row completed with X pieces when placing an X on the position 3
- **Then** Player x is declared as the winner 

---

### Scenario: Player O wins a line
- **Given** Player O took the positions 1,4 and 7 
- **When**   Player O place the piece on the position 7 gets a full row completed
- **Then**  Player O is declared the winner

---

### Scenario: Diagonal rows 
- **Given** Player X has X's on the positions 1 and 5  
- **When** Player X placed an X on the position 9  
- **Then** Player X wins by gaining a diagonal row

---

### Scenario: The match ends in a draw
- **Given** Dashboard is almost full, has only one position left  
- **When** The player X places a piece on the last position left, but this doesnt generates a full row of X's  
- **Then** the match ended in a draw, no one wins

---

### Scenario: After a Player gets a full row
- **Given**  The player with the full row wins  
- **When** The dashboard gets locked so the other player isn't able to place a piece 
- **Then** The game shows the winner it can be Player X or Player O, depending on who gets a full row

---

### Scenario: Reset the dashboard
- **Given** a Player wins or the match ends in a draw  
- **When** Player can reset the game by clicking on "New match" or exit
- **Then** If the player clicks "New match" a clean dashboard show up, if the player clicks exit the window closes 

### Scenario: Player chooses to play vs a person
- **Given** The game asks against who the player wants to play  
- **When** Player chooses the option agains a person
- **Then**  The game switch between players after one player places a piece on a position

### Scenario: Player chooses to play vs a boot
- **Given**  The game asks against who the player wants to play 
- **When** Player chooses the option agains a boot
- **Then** The boot places a piece right after the Player placed its own piece.



