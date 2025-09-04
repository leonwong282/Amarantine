# Copilot Instructions for Amarantine (Ren'Py Visual Novel)

## Project Overview
- This is a Ren'Py-based visual novel project. All game logic, story, and assets are managed under the `game/` directory.
- The main script is `game/script.rpy`, which contains the story, character definitions, and scene transitions.
- Images, audio, and GUI assets are organized in subfolders: `images/`, `audio/`, and `gui/`.

## Key Files & Structure
- `game/script.rpy`: Main scenario and dialogue. Follows Ren'Py syntax and conventions.
- `game/options.rpy`, `game/screens.rpy`, `game/gui.rpy`: Configure game options, UI screens, and GUI elements.
- `game/images/`: Backgrounds, character sprites, icons. Filenames like `bg 01.png` are referenced directly in script.
- `game/audio/`: Music and sound effects, referenced in script with `play music` and `play sound`.

## Coding Patterns & Conventions
- Character definitions use `define <short> = Character("Name")` at the top of `script.rpy`.
- Scene transitions use `scene <bg>` and `with Dissolve(<seconds>)` for visual effects.
- Dialogue lines are written as either plain strings (narration) or `<short> "text"` (character speech).
- Music and sound: Use `play music "audio/filename.mp3"` and `play sound "audio/filename.mp3"`.
- Comments are in Chinese, code in Ren'Py script format.
- Story is linear, with some choices and branching handled directly in the script.

## Developer Workflow
- Edit `.rpy` files in `game/` for story, logic, and configuration.
- Add new assets to `images/` or `audio/` and reference them by filename in the script.
- To test changes, launch the Ren'Py launcher and run the project. No build step is required; Ren'Py compiles scripts automatically.
- Save files are in `game/saves/`.

## Integration & External Dependencies
- No external Python packages or custom modules are used; all logic is in Ren'Py script.
- Fonts (e.g., `SourceHanSansLite.ttf`) are placed in `game/` and referenced in GUI config files.

## Example Patterns
```renpy
# Character definition
define y = Character("云锦")

# Scene transition
scene bg 01
with Dissolve(.5)

# Dialogue
y "“如果能像飞鸟一样，自由地翱翔在天空，该有多好。”"

# Play music
play music "audio/bg0.mp3" fadeout 1.0 fadeout 1.0
```

## Tips for AI Agents
- Always use asset filenames as they appear in `images/` and `audio/`.
- Maintain story flow and character consistency; follow the established style in `script.rpy`.
- When adding new scenes or choices, use Ren'Py's label and jump syntax.
- Do not introduce Python code unless editing Ren'Py's Python blocks (rare in this project).

---
If any section is unclear or missing, please provide feedback so this guide can be improved for future AI coding agents.
