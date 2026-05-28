# 🎄 Christmas Text Adventure — C++

A console-based text adventure game written in C++ where you play as a hero chosen by the Three Wise Kings to deliver special gifts (Wi-Fi, a smartphone, and C++ books) to baby Jesus. Your journey spans five chapters of branching paths, random encounters, and meaningful choices that determine your fate.

---

## Features

- Interactive narrative split into five story chapters
- Branching path choices at each chapter (3 options per crossroads)
- Random encounter system with 14 possible events — enemies, treasures, shields, and more
- Health, shield, and score tracking throughout the game
- Three difficulty levels that adjust starting stats
- Persistent leaderboard saved to a local file (`puntajes.txt`)
- Simple console UI with screen clearing and a status bar

---

## Requirements

- C++ compiler (`g++` recommended)
- Compatible with Linux, Windows, macOS, or any environment with a C++ toolchain

---

## Compilation

```bash
g++ text-adventure-christmas.cpp -o christmas-adventure
```

---

## Running the Game

```bash
# Linux / macOS
./christmas-adventure

# Windows
christmas-adventure.exe
```

---

## Main Menu

| Option | Description          |
|--------|----------------------|
| 1      | Start a new game     |
| 2      | View leaderboard     |
| 3      | Exit                 |

---

## Difficulty Levels

Chosen at the start of each run. Difficulty affects your starting lives and whether you begin with a shield.

| Difficulty                          | Score | Lives | Shield |
|-------------------------------------|-------|-------|--------|
| Easy — Camino del Encanto           | 5000  | 2     | ✅     |
| Medium — Bosque Mágico              | 5000  | 2     | ❌     |
| Hard — Duendes y Escarpos           | 5000  | 1     | ❌     |

---

## Gameplay

Each chapter presents a crossroads with three paths. After choosing, a random encounter triggers — you may gain or lose points, lives, or shields. The status bar updates after every event:

```
-----------------------------------------------------
|Puntaje: 4000       Ptos de vida: 1       Escudo: 1|
-----------------------------------------------------
```

Survive all five chapters to win. Lose all lives and the run ends early.

### Random Encounters

| Type     | Examples                                      | Effect              |
|----------|-----------------------------------------------|---------------------|
| Enemies  | Zombie, Dragon, Cyclops, Giant Spider, Bandit | −1 or −2 lives / −1000 pts |
| Rewards  | Treasure, Ancient Scroll, Gold, XP            | +1000 pts           |
| Pickups  | Armor, Shield, Extra Life                     | +1 shield / +1 life |

Shields absorb damage before lives are deducted.

---

## Score & Leaderboard

At the end of each run (win or lose) your name and score are appended to `puntajes.txt`. You can view all saved scores from the main menu.

```
David    5000
Juan     4000
```

---

## Project Structure

```
text-adventure-christmas.cpp   # Full game source
puntajes.txt                   # Auto-generated score log (created on first run)
```

---

## Known Limitations & Potential Improvements

- [ ] Refactor global state into a `Player` struct or class
- [ ] Translate all in-game text to English
- [ ] Add input validation for name entry
- [ ] Implement a proper leaderboard (sorted, with timestamps)
- [ ] Add replay and exit confirmation prompts
- [ ] Replace raw `\033[2J` escape codes with a cross-platform clear-screen utility

---

## Author

**Santiago David Castillo**  
Computer Science Engineering Student  
[GitHub](https://github.com/Santiago193)

---

## License

MIT © Santiago David Castillo
