# CV Contents:

1. I am Zavodova Alina

2. My *email* alinaxavod@gmail.com and *GitHub* https://github.com/AlinaZav

3. _I am a student at RS-school._ I am studying _*frontend development*_ in JS. My goal is to learn the basics of development in a short period of time and get a **dream job**. _My strengths are: persistence, hard work and learning ability._

4. I have **HTML** and **CSS** layout skills, and minimal knowledge of **JavaScript**.

5. *Code Examples my game Tic-Tac-Toe*.\
```javascript
let currentPlayer = 'X';
let gameBoard = ['','','','','','','','',''];
let gameActive = true;

function handlePlayerTurn(clickedCellIndex) {
    if(gameBoard[clickedCellIndex]!== '' || !gameActive){
        return;
    }
    gameBoard[clickedCellIndex] = currentPlayer;
    checkForWinOrDraw();
    currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
}

function cellClicked(clickedCellEvent) {
    const clickedCell = clickedCellEvent.target;
    const clickedCellIndex = parseInt(clickedCell.id.replace('cell-', '')) - 1;
    if (gameBoard[clickedCellIndex] !== '' || !gameActive){
        return;
    }
    handlePlayerTurn(clickedCellIndex);
    updateUI();
}
const cells = document.querySelectorAll('.cell');

cells.forEach(cell => {
    cell.addEventListener('click', cellClicked, false);
});

function updateUI() {
    for(let i = 0; i < cells.length; i++) {
        cells[i].innerText = gameBoard[i];
    }
}
function announceWinner(player) {
    const messageElement = document.getElementById('gameMessage');
    const Tuturu = document.getElementById('tuturu');
    Tuturu.play();
    messageElement.innerText = `Player ${player} Wins!`;

  }

  function announceDraw() {
    const messageElement = document.getElementById('gameMessage');
    messageElement.innerText = 'Game Draw!';
  }
const winConditions = [
    [0, 1, 2], // Top row
    [3, 4, 5], // Middle row
    [6, 7, 8], // Bottom row
    [0, 3, 6], // Left column
    [1, 4, 7], // Middle column
    [2, 5, 8], // Right column
    [0, 4, 8], // Left-to-right diagonal
    [2, 4, 6]  // Right-to-left diagonal
  ];

  function checkForWinOrDraw() {
    let roundWon = false;

    for (let i = 0; i < winConditions.length; i++) {
        const [a, b, c] = winConditions[i];
        if (gameBoard[a] && gameBoard[a] === gameBoard[b] && gameBoard[a] === gameBoard[c]) {
            roundWon = true;
            break;
        }
    }

    if (roundWon) {
        announceWinner(currentPlayer);
        gameActive = false;
        return;
    }

    let roundDraw = !gameBoard.includes('');
    if (roundDraw) {
        announceDraw();
        gameActive = false;
        return;
    }
  }
  ```

![image T-T-T](https://github.com/user-attachments/assets/6c489644-b089-485e-831b-7b4f148ce38d)

6. I have no experience in commercial development, *but I have various pet projects that I wrote during my self-study process.*  **View by https://github.com/AlinaZav**

7. >My English proficiency level A1.