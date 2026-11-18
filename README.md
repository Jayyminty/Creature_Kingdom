# Creature Battle Project (OOP + Git Branching Practice)

This project is designed to help me learn **object-oriented programming** in Python — especially **inheritance** — while also practicing key **Git concepts** like branching, merging, conflict resolution, and version history.

I will begin with a base class (`Creature`) and create additional subclasses on separate Git branches to simulate a real development workflow.

---

## Learning Objectives

### Python / OOP
- Understand and implement **classes**
- Use **inheritance** to extend behaviors
- Override and extend methods (e.g., `attack()`)
- Practice writing simple test code in `main`

### Git / Version Control
- Create and switch branches
- Merge branches into `main`
- Resolve merge conflicts
- View commit history (`git log --all --graph`)

---

## Project Structure

    oop_creature_code/
    |
    |-- creature_simulation.py   # Base class + subclasses
    |-- README.md                # This file

## Class Design

- `Creature` (base class): attributes `name`, `hp`, `attack_power`; methods `attack(target)` and `is_alive()`.
- `FlyingCreature(Creature)` (branch `flying_creature`): adds `altitude` and `fly_to(new_altitude)`; `attack()` is overridden so the creature attacks from above.
- `SwimmingCreature(Creature)` (branch `swimming_creature`): adds `depth` and `dive_to(new_depth)`; `attack()` is overridden so the creature attacks from underwater.
- `FireCreature(Creature)` (branch `fire_creature`): adds `fire_level` (0-100) and `emit_fire(new_fire_level)`; `attack()` is overridden so the fire level adds bonus damage.

## How to Test and Run

1. Make sure Python 3 is installed.
2. Open a terminal in the `oop_creature_code` folder.
3. Run: `python3 creature_simulation.py`
4. The test code at the bottom of the file (`if __name__ == "__main__":`) runs automatically. It tests `Creature`, `FlyingCreature`, `SwimmingCreature` and `FireCreature`, and prints the expected value next to the actual value for each test.
5. To see the Git history, run: `git log --all --graph`
