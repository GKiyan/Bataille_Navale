# Bataille Navale

A Battleship game in Java, playable in the terminal or with a Swing GUI, against a human or an AI.

## Features

- **Two modes**: graphical interface (Swing) or terminal.
- **Several player types**:
  - `Utilisateur`: a human player
  - `RandomPlayer`: shoots at random cells
  - `AIPlayer`: hunts at random, then follows the directions around a hit to sink the ship
- **AI vs AI** games in terminal mode.
- **Configurable rules** in `config.properties`: number and sizes of ships, board size, display settings.

## Project structure

```
src/bataille/
├── Jeu.java        # Entry point: mode and player selection
├── Config.java     # Loads and validates config.properties
├── game/           # Board and boats
├── player/         # Player types (human, random, AI)
├── view/           # Swing GUI (view + controller)
├── addon/          # Cells and positions
└── exception/      # Configuration errors
```

## Build and run

Requires Java 17+. Run from the repository root, so that `config.properties` is found:

```bash
javac -d out $(find src -name "*.java")
java -cp out bataille.Jeu
```

## Configuration

```properties
nbBateau=3              # number of ships
tailleBateau=5,4,3      # size of each ship
tailleTabLargeur=10     # board width
tailleTabLongueur=10    # board height
```
