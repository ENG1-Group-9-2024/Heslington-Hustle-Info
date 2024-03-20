# Player performs an activity

Primary Actor: Player

Supporting Actors: N/A

Precondition: Less than seven in-game days have elapsed.

Trigger: Player selects a location on the map to interact with

Main Success Scenario:
- The player performs the activity available at the selected location
- The system records the activity performed, so it can compute the score
- The player’s energy is decreased as appropriate.
- In game time moves forward the appropriate amount.

Secondary Scenario:
- The player does not have enough energy or time left to perform the activity. They are informed as such.

Success Postcondition: The player is able to perform the selected activity.

Minimal Postcondition: The player has zero or more energy and the in-game time elapsed for the day has not exceeded 16 hours.

# Player moves around the map
Primary Actor: Player

Supporting Actors: N/A

Precondition: Less than seven in-game days have elapsed.

Trigger: Player uses an input device (keyboard / mouse) to control the character.

Main Success Scenario:
- The system recognises the input as valid.
- The player’s current location permits them to move in the desired direction.
- The character moves across the screen according to the input.

Secondary Scenarios:
- 1
  - The game does not recognise the input.
  - The game state does not change

- 2
  - The input is not permitted as there are no routes that the player can follow in the specified direction.
  - The game state does not change

Success Postcondition: The player can move across the map in such a way that they can visit every activity.

Minimal Postcondition: The player is always visible on the screen

# Game over
Primary Actor: Player

Supporting Actors: N/A

Precondition: Exactly 7 in-game days have elapsed.

Trigger: Player sleeps at the end of the seventh day.

Main Success Scenario:
- The player is presented with a game-over screen, informing them of their score, and possibly offering suggestions for how they can do better next time.

Postcondition: The game is over
