# Welcome to My Page

Right now everything here is fairly temporary. Ideally this page wouldn't be using a template theme, but that's just the way it is right now.

## Who Am I?

| Name          | Tanner Sundwall                                 |
|:--------------|:------------------------------------------------|
| **College**   | Portland State University                       |
| **Degree**    | B.S.                                            |
| **Major**     | Computer Science                                |
| **Languages** | C, C++, C#, Rust, Java, JavaScript, Python, SQL |
| **Email**     | sundwalltanner@gmail.com                        |
| **GitHub**    | [github.com/sundwalltanner](https://github.com/sundwalltanner) |
| **LinkedIn**  | [linkedin.com/in/tanner-sundwall](https://www.linkedin.com/in/tanner-sundwall/) |

## Projects

### Nonogram Puzzle Game Remade in React.js

**Date:** March 2020 - Ongoing

**Language(s):** JavaScript

**Repository:** [github.com/Sundwalltanner/React-Nonogram](https://github.com/Sundwalltanner/React-Nonogram)

**Technologies:** React.js

**Description:** While looking for a post-college job, I've been working on remaking my Rust Nonogram game in a format more easily accessible. I'm trying to remake the entirety of the original game I made and then some using JavaScript, the React library, and GitHub Pages as a host.

The game is currently playable here: [sundwalltanner.github.io/React-Nonogram/](https://sundwalltanner.github.io/React-Nonogram/)

**It's still a work in progress**

### Portland State University Capstone Burning Man Project

**Date:** September 2019 - March 2020

**Language(s):** Python

**Repository:** [gitlab.com/madelyea/team-visualizer](https://gitlab.com/madelyea/team-visualizer)

**Technologies:** Raspberry Pi 4, Raspbian OS, VirtualBox, Debian Buster OS, Network Sockets, VLC, D-Bus, Git, GitLab, Draw.io

**Description:** This project was started and completed over the course of the last two terms I spent working on my B.S. in Computer Science at Portland State University. During the first term, students in the course elected themselves as candidates to become team leads, and after a couple weeks of vetting, some were chosen to be the team leads of groups of six other Computer Science students enrolled in the course. We did group interviews with the team leads, and in the end, the team leads formed their own groups based on these interviews.

After groups were chosen, sponsors from around Portland presented potential projects in front of the class. We then went through a process that eventually landed us the ```Burning Man Project```.

The goal of the ```Burning Man Project``` was to create a program using Python that would play a randomized playlist made up of videos placed on the storage device of a Raspberry Pi 4 on boot, trim potential intro and outro credits from videos that were over a certain length, automatically shutdown at a certain time, and allow for certain mouse-specific keybindings, syncing all of this with another Raspberry Pi 4 using just an ethernet cable.

In the end we ended up with software that starts on boot on a Raspberry Pi 4, randomizes a playlist made up of videos placed in a certain directory, trims from the start and end of videos based on their length, boots the playlist up in VLC, assigns itself as a parent or child depending on certain conditions (mouse connected, another Pi connected via ethernet, etc...), and listens for commands based on whether it's considered a parent or child. If it's a parent, it listens for mouse commands. If it's a child, it listens for commands from the parent.

We also produced enough documentation such that our sponsor would be able to walk through the steps necessary to get from a fresh Raspberry Pi 4 to one that starts our software correctly on boot. This was necessary due to the fact that this would be run at a camp at Burning Man, and the Pis themselves were expendable. This meant we also had to automate as much of the setup as we possibly could in order to make setting up a fresh Pi easier.

### Nonogram Puzzle Game

**Date:** January 2020 - February 2020

**Language(s):** Rust

**Repository:** [github.com/sundwalltanner/rust-nonogram](https://github.com/Sundwalltanner/Rust-Nonogram)

**Technologies:** Piston modular game engine, Git, GitHub, JSON

**Description:** Nonograms are similar to Sudoku. They're just another number-based puzzle game. The goal is to use the hint numbers alongside the rows and columns of the game board in order to determine which cells need to be filled in. If the correct cells are filled in, you win.

This is the project I've spent the most time programming at this point. I spent more time working on the ```Burning Man Project``` above, but that's just due to the fact that we were given more time to work on it, and it was a larger group-based project.

This was made as my final project for the one and only Rust course I took at Portland State University.

The gif below says a lot about the final product that I can't:

![Gif of solving 5x5 Nonogram](https://i.imgur.com/wxxDn44.gif)

Currently, this program features:
* Randomly generated Nonogram puzzles of varying dimensions.
* Dropdown menu allowing user to change dimensions of generated board.
* Button allowing user to generate a new board.
* Mouse keybindings:
    * ```Left click``` mouse to fill boxes and interact with buttons.
        * Support for ```left click hold``` to dynamically perform functions based on first box interacted with.
    * ```Right click``` mouse to mark boxes.
        * Support for ```right click hold``` to dynamically perform functions based on first box interacted with.
* Keyboard keybindings:
    * ```J key``` to fill boxes.
    * ```K key``` to mark boxes.
    * ```Up key``` to increase dimensions.
    * ```Down key``` to decrease dimensions.
    * ```R key``` to restart and generate a new board.
* Stats screen upon puzzle completion with option to start again.
    * In-game timer, with final completion time displayed at the end.
    * Puzzle complexity parameters such as filled / unfilled ratio.
* Progress automatically saved in ```savedata.json``` file when program is exited.

It was a lot of fun to work on, and hopefully I find time to come back around to it and work on it some more. I've got a pretty big list of features I could potentially add to it at the end of the README.md in its repository.

### ASCII Chess

**Date:** March 2019

**Language(s):** C++

**Repository:** [github.com/sundwalltanner/ascii-chess](https://github.com/Sundwalltanner/Ascii-Chess)

**Technologies:** Nothing fancy

**Description:** Uses a whole lot of C++ in order to produce a fully playable chess game from within the terminal. This supports everything you'd expect in a chess game except for AI, pawn promotions, castling, and en passant.

It was a lot more difficult to make than I initially thought it would be largely due to the win condition of chess not being as simple as ```capture the other player's king```. This doesn't allow a player to make an illegal move, be it a move that that piece just simply isn't allowed to make in accordance with the rules of chess, or that it renders one's own king vulnerable to attack. The game's logic needs to look ahead at a lot of different things in order for this to work.

Basically, this is what the game should look like in your terminal:

![Chess tutorial image #1](https://i.imgur.com/GYG7nGS.png)

In the image above, I've entered ```a2 a4```. This means that I want to move the white's leftmost pawn forward two spaces.

![Chess tutorial image #2](https://i.imgur.com/wi67VVp.png)

Success! As you can see in the image above. The white's leftmost pawn was successfully moved forward two spaces, and it's now black's turn.
