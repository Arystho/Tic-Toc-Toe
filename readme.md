AI versus IA

-Faites en sorte que l'IA joue contre elle même.

Ce qui est attendu :

-Vous devez avoir un bouton qui permet de lancer les parties
-L'ia doit relancer automatiquement une nouvelle partie
-A chaque coup, l'ia doit "réfléchir" entre 0 et 750ms
-Vous devez avoir un bouton qui permet de stopper les parties



Js:

AI vs IA

=======================================================
//fonction qui permet de de changer de joueur
function changePlayer(){
    currentPlayer = currentPlayer === 1 ? 2: 1;
}

function playWithAI(){
    if (stopgameFlag) return;

    let randomIndex = math.floor(math.random() * 9);
    while (grid[randomIndex] !== 0) {
        randomIndex = mathf,floor(math.random() * 9);
    }
}

grid[randomIndex] = currentPlayer;
displayPlayerSymbol(randomIndex);
checkIfSomeoneWon();

if(!isGameWon && !isGameFinished){
    changePlayer();
    setTimeout(playWithAI, math.random() * 750);
} else if (isGameFinished){
    setTimeout(newGame, 750)
}

function newGame(){
    currentPlayer = 1;
    isGameWon = false;
    isGameFinished = false
    grid = [0, 0, 0, 
            0, 0, 0, 
            0, 0, 0];

    document.querySelectorAll('.cell').forEach(cell => {
        cell.innerHTML = '';
    });
    setTimeout(playWithAI, 750);
}

function startGame(){
    stopgameFlag = false;
    newGame()
}

function stopgame() {
    stopgameFlag = true;
}


========================================================


