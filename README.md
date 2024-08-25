Simple Game project using AVR Atmega32 with Keypad and LCD. The game involves solving basic arithmetic equations within a time limit of 10 seconds per level. The player is presented with equations and has to input the correct answer within the time limit.
Here's a breakdown of the code:

Initialization:

The code initializes the LCD, keypad, and Timer/Counter 0 (TIMER0) in CTC mode with interrupts enabled.

Game Logic:

The game presents three math puzzles sequentially to the player.

Each puzzle is displayed on the LCD screen with a missing number represented by "??".

The player has to input the correct number using the keypad before the time limit (10 seconds) for each level expires.

The player score is updated based on the correctness and timeliness of their answers.

Level Progression:

If the player solves a puzzle correctly within the time limit, they proceed to the next level.

If the player answers incorrectly or runs out of time, the game ends, and the final score is displayed.

Timer Configuration:

The timer is likely configured to run at a certain frequency determined by the system clock (in this case, 8 MHz).

By adjusting the compare value and the timer prescaler, you can control the duration of the timer interrupt, which in turn controls the timing aspects of the game.

Interrupt Service Routine (ISR):

The TIMER0_COMP_vect ISR increments the flag1 variable, which is used to track the elapsed time for each level.

User Interface:

The LCD shows the math puzzles and feedback messages based on the player's input and performance.

The keypad is used for user input to solve the puzzles.
