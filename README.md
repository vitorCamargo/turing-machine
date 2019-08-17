# Turing Machine
👨🏽‍💻👏 Assignments for 'Formal Languages, Automata and Computability' subject about a simulation of Turing Machine.

## More Information
This project is developed using the programming language Python3, however, the speaking language was Portuguese.

### Introduction
The program was developed by [Vitor Camargo](https://github.com/vitorCamargo), [Thaís Zorawski](https://github.com/TZorawski), [Cláudia Sampedro](https://github.com/claudiaps) and [Lucas Ribeiro](https://github.com/lucasvribeiro), students of the Bachelor of Computer Science course at the Federal Technological University of Paraná - *campus* Campo Mourão (UTFPR-CM). This program was developed in the semester 2018/2, for the discipline Formal Languages, Automata and Computability, taught by Professor [Marco Aurélio Graciotto Silva](https://github.com/magsilva), from the Computing Department of UTFPR-CM (DACOM).

### About Turing Machine
A *Turing Machine* is a theoretical model of a machine that manipulates symbols on a tape according to a set of rules and transitions. A Turing machine has an alphabet, which will be the machine-acceptable set of symbols, a set of possible states, one or more tapes, and a set of transitions that indicate what will happen to the machine and the tape according to value that is read at the current tape position.

### How the Program Works
- The program in question is divided into two files: ***main.py*** and ***turingMachine.py***. The *main.py* file is responsible for reading the text file containing the machine, reading the tape given as input, and calling the execution of the *turingMachine.py* file that contains all the logic of operating a Turing Machine. The approach used to implement the machine was to insert each transition into an object and save the transitions in a *queue* using the wide search.

- The instruction format for program execution is:  
	    `python main.py “turingMachine.txt” “tape”`
    
  **Example:**  
  `python main.py examples/has1.jff.txt 001100`

- For testing, in the *"examples"* directory of this repository there are some examples of files with Turing Machines in the format that should be used as input to the program.

- The program output format is:  
  `{'tape', 'current_state', 'head_tape', 'counter': 497}`

  Where *'tape'* indicates the final tape content, *'current_state'* indicates the state the machine is in at the end of execution, *'head_tape'* indicates the final position of the tape head and *'counter'* is the counter to prevent the machine from going into infinite *loop*.
  
  In addition, at the exit of the program there will be a line indicating the final result of the Machine execution, which can be:
  `0: Computing done and accepted.`  
  `-1: Computation terminated and rejected.`  
  `-2: Computation didn't terminate. (Looping Interruption)`  
  `-3: Incorrect tape value inserted.`

  **Output Example:**  
  `0: Computing done and accepted.`  
  `{'tape': 'BBB1001010101', 'current_state': '1', 'head_tape': 3, 'counter': 497}`
  
- To convert Turing Machines from *.jff* to *.txt* (format supported by the program), use the *jflap-pda2utfpr.py* file as follows:

  `python jflap-turing2utfpr.py turingMachine.jff turingMachine.txt`
  
