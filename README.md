## Project Goal

The goal of this project is to create a program to find a path through a maze loaded from a text file. The maze is represented in a file with designated points:

- Entrance point ("P")
- Exit point ("K")
- Walls ("X")
- Walkable spaces (blank spaces)

## Example 10x10 Maze Format:
```
XXXXXXXXXXXXXXXXXXXXX
P           X     X X
XXX XXX XXX X XXX X X
X X X   X X   X X X X
X XXX XXX XXXXX X X X
X X   X       X   X X
X X XXX XXX X X XXX X
X   X X X   X X X   X
XXXXX X X XXX X X X X
X     X X X X X X X X
X XXXXX X X X X X X X
X X     X X   X   X X
X X XXXXX X XXXXXXX X
X   X   X X   X     X
X XXXXX X XXX X XXXXX
X X     X X   X   X X
X X X XXX XXXXXXX X X
X   X X   X     X   X
XXXXX X XXX XXX XXX X
X     X       X     K
XXXXXXXXXXXXXXXXXXXXX
```

## Maze Size Requirements

The maximum maze size is 1024 x 1024, calculated by passable paths.

## Program Compilation and Execution

The program can be compiled using a Makefile, which includes compilation rules and instructions for linking files into the final executable file. To compile the program, simply run the `make` command in the directory containing the Makefile. 

After compilation, go to the `exe` directory and run the program, specifying the maze file name:

### Available Launch Parameters
- `-f [filename.txt]` – required parameter; specifies the input file, which must be a correctly formatted maze file.
- `-o [filename.txt]` – optional parameter; saves the program’s output to the specified file (if the file does not exist, it will be created).
- `-h` – optional parameter; displays a brief help message about program usage.

## Example Program Execution
```
 ./maze -f ../default_maps/10x10.txt -o last_test.txt
```

```
XXXXXXXXXXXXXXXXXXXXX
P           X     X X
XXX XXX XXX X XXX X X
X X X   X X   X X X X
X XXX XXX XXXXX X X X
X X   X       X   X X
X X XXX XXX X X XXX X
X   X X X   X X X   X
XXXXX X X XXX X X X X
X     X X X X X X X X
X XXXXX X X X X X X X
X X     X X   X   X X
X X XXXXX X XXXXXXX X
X   X   X X   X     X
X XXXXX X XXX X XXXXX
X X     X X   X   X X
X X X XXX XXXXXXX X X
X   X X   X     X   X
XXXXX X XXX XXX XXX X
X     X       X     K
XXXXXXXXXXXXXXXXXXXXX
```

Example movement output:
```
FORWARD 11
TURNRIGHT
FORWARD 2
TURNLEFT
FORWARD 2
TURNLEFT
FORWARD 2
TURNRIGHT
FORWARD 4
TURNRIGHT
FORWARD 4
TURNRIGHT
FORWARD 2
TURNLEFT
FORWARD 6
TURNLEFT
FORWARD 2
TURNLEFT
FORWARD 4
TURNRIGHT
FORWARD 2
TURNRIGHT
FORWARD 6
TURNRIGHT
FORWARD 4
TURNLEFT
FORWARD 2
TURNLEFT
FORWARD 2
TURNRIGHT
FORWARD 2
TURNLEFT
FORWARD 2
TURNRIGHT
FORWARD 2
TURNLEFT
FORWARD 1
```
