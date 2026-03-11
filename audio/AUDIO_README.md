# Qubit Defense - Audio Sound Effects Requirements

This document outlines all the sound effects needed for the Qubit Defense game. Place all sound files in the `audio/` folder as MP3 files.

## Sound File Naming Convention
All sound files should be named exactly as listed below and saved as `.mp3` format in the `audio/` folder.

---

## Game State Sounds

| Sound Name | File Name | Description | Suggested Characteristics |
|------------|-----------|-------------|--------------------------|
| Game Over | `game_over.mp3` | Played when player loses all lives | Dramatic, descending tone, 2-3 seconds | DONE
| Victory | `victory.mp3` | Played when player completes all waves | Triumphant, celebratory, 3-5 seconds | DONE
| Wave Start | `wave_start.mp3` | Played when a new wave begins | Alert, ascending, 1-2 seconds | DONE
| Wave Complete | `wave_complete.mp3` | Played when a wave is cleared | Satisfying completion sound, 1-2 seconds | DONE

---

## Tower Sounds

| Sound Name | File Name | Description | Suggested Characteristics |
|------------|-----------|-------------|--------------------------|
| Tower Place | `tower_place.mp3` | Played when a tower is placed | Mechanical, satisfying click, 0.5 seconds | DONE
| Tower Remove | `tower_remove.mp3` | Played when a tower is removed (right-click) | Reverse mechanical sound, 0.5 seconds | DONE |
---

## Enemy Sounds

| Sound Name | File Name | Description | Suggested Characteristics |
|------------|-----------|-------------|--------------------------|
| Enemy Kill | `enemy_kill.mp3` | Played when enemy is killed | Satisfying destruction, 0.5-1 second | DONE
| Enemy Survive | `enemy_survive.mp3` | Played when enemy survives measurement | Disappointing hum, 0.5 seconds | DONE

---

## Quantum Effect Sounds

| Sound Name | File Name | Description | Suggested Characteristics |
|------------|-----------|-------------|--------------------------|
| Gate Apply | `gate_apply.mp3` | Played when quantum gate is applied | Sci-fi blip, electronic tone, 0.3 seconds | DONE
| Measurement | `measurement.mp3` | Played when measurement tower fires | Scanning/reading sound, 0.5-1 second |
| Collapse | `collapse.mp3` | Played when wavefunction collapses | Whoosh/implosion effect, 0.5 seconds |
| Superposition | `superposition.mp3` | Optional: ambient quantum effect | Ethereal hum (not currently implemented) |

---

## UI Sounds

| Sound Name | File Name | Description | Suggested Characteristics |
|------------|-----------|-------------|--------------------------|
| Button Click | `button_click.mp3` | General button press | Soft click, 0.2 seconds | DONE
| Button Hover | `button_hover.mp3` | Button hovered over | Subtle hover sound, 0.1 seconds | DONE
| Error | `error.mp3` | Invalid action (not enough credits, etc.) | Negative buzz, 0.3 seconds | DONE
| Life Lost | `life_lost.mp3` | Played when an enemy escapes | Warning/alarm, 0.5 seconds | DONE

---

## Volume Recommendations

The audio system uses category-based volume control:
- **Music**: 50% default volume
- **SFX**: 70% default volume  
- **UI**: 50% default volume
- **Quantum**: 60% default volume

Individual sound effects can have their volume adjusted in the code (typically 0.3-1.0 range).

---

## Adding New Sounds

To add or modify sounds:

1. Add the sound file to the `audio/` folder
2. Update the `SOUND_EFFECTS` object in `js/audio.js` if needed
3. The sound will automatically be loaded and available via `playSound('soundName')`

---

## Testing

When adding sound files, test:
- Volume levels are balanced
- Sounds play without distortion
- Multiple overlapping sounds don't cause issues
- Browser autoplay policies are handled (user must interact with page first)
