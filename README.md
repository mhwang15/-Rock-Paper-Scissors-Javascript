# -Rock-Paper-Scissors-Javascript

//Prompts user for input. (rock, paper or scissors)
const getUserChoice = (userInput) => {
  userInput = prompt ('What do you choose?');
  
  if (userInput === 'paper' || userInput === 'rock' || userInput ==='scissors') {
    return userInput;
  } else {
    console.log('Error!');
  }  
};
//Computer randomly generates rock, paper or scissors
const getComputerChoice = () => {
  switch (Math.floor(Math.random()*3)) {
    case 0:
      return 'rock';
      break;
    case 1:
      return 'paper';
      break;
    case 2:
      return 'scissors';
      break;
    }
};
//Winner is determined
const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice) {
    return 'The game was a tie.';
  } else if (userChoice === 'rock') {
    if (computerChoice === 'scissors') {
      return 'You win!';
  } else {
    return 'Uh oh! The computer won!';
  }
  } else if (userChoice === 'paper') {
    if (computerChoice === 'rock') {
      return 'You win!';
    } else {
      return 'Uh oh! The computer won!';
    }
    } else if (userChoice = 'scissors') {
      if (computerChoice = 'paper') {
        return 'You win!';
      } else {
        return 'Uh oh! The computer won!';
      }
    }
  }
//play game
const playGame = () => {
  const userChoice = getUserChoice('paper', 'rock', 'scissors');
  const computerChoice = getComputerChoice();
  console.log('You threw: ' + userChoice);
  console.log('The computer threw: ' + computerChoice);
  console.log(determineWinner(userChoice, computerChoice));
}

playGame();
