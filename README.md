# heist-squad-bot

Heist Squad Bot is a Telegram strategy game created as a Python group project.  
The user builds a team of four characters and completes missions with different difficulty levels.

## Project Description

The main idea of the game is that the strongest team is not always the best team.  
The player needs to create a balanced team with different roles and enough skills for the selected mission.

The bot gives the player 8 random characters. Each character has a role, rarity, and four skills:

- Hack
- Fight
- Stealth
- Strategy

The player chooses exactly 4 characters. After that, the bot evaluates the team and shows the final result.

## Features

- Telegram bot interface
- Inline keyboard buttons
- Three mission difficulty levels: Easy, Medium, Hard
- Random character selection
- Character roles and rarity
- Team balance checking
- Skill balancing system
- Mission requirements
- Score calculation
- Random events
- Leaderboard
- Error handling for wrong text commands and invalid team size

## Game Logic

The game checks two types of balance:

### 1. Team composition balance

A balanced team should:

- have at least 3 different roles
- not be too weak
- not be too overpowered

Balanced team composition gives +15 points.  
Unbalanced team composition gives -10 points.

### 2. Skill balance

For each mission skill, the bot compares the team's skill value with the mission requirement.

Scoring system:

- Too low skill = +8 points
- Balanced skill = +20 points
- Overpowered skill = +12 points

This means the bot does not simply reward the highest numbers.  
The goal is to build a team that fits the mission requirements.

## Mission Levels

The bot has three missions:

### Easy
School Data Rescue

### Medium
Museum Heist

### Hard
Cyber Bank Mission

Each mission has different required values for Hack, Fight, Stealth, and Strategy.

## Random Events

After team evaluation, the bot adds a random event.  
A random event can increase or decrease the final score.

Examples:

- Security system was weak
- Unexpected guard appeared
- Team found a secret shortcut
- Communication problem happened

## Technologies Used

- Python
- pytelegrambotapi
- Google Colab
- Telegram Bot API
- GitHub

## Bot Commands

/start - start the bot  
/menu - open the main menu  
/help - show game instructions

## How to Run the Project

1. Install the required library:

```python
pip install pytelegrambotapi
