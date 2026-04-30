# GDIM 33 In-Class Activities
## W1
### Activity 1
Not present


### Activity 2
Not present


## W2
No Devlog for this week


## W3
### Activity 1
<img width="1880" height="1441" alt="honse  Breakdown" src="https://github.com/user-attachments/assets/fbbe5540-3bf7-413b-a19f-6d53edf0a5f8" />

### Activity 2

1. Saving the event name as a scene variable helps save time by not needing to copy the event name in the custom event and trigger custom event. This could help even more if there are multiple graphs that are triggering the same custom event. 
2. Using debug.Log nodes to check whether or not my transitions worked helped me see if there were any issues with my state transitions. If I was able to see the log, my transition was working. It also helped me see if an issue was caused in my transition or on a state.
3. The set cursor lock state doesn't seem like something that would be useful for my Vertical Slice. Since my game is a papers, please like, the player will be clicking and dragging and the mouse needs to remain visible for that. There aren't many points in my game where the mouse needs to be hidden or locked.
4. The only part of my game where I could see a game state be useful is to differentiate between the core gameplay, being looking at the horses and their documents, and the final results screen that shows how the player did. This is to prevent anymore horses from showing up and causing issues behind the report.

## W4
### Activity 1
Goal: Test the controls (clicking and dragging) and see if the controls feel good. 


Playtest Team: Kaleb Reyes, Sebastian Magana, Frances Kim, Jess Tran, Rebecca Feng, Landon Her


Notes:
- Make sure the IDs can’t be moved out of bounds
- Controls feel good
- Fix ID layering issues


### Activity 2
1. Yes because all that is needed to add more dialogue is to create a new scriptable object and hook it up to the replies that you want. There isn't a need to go through any code for the writer.
2. There isn't a limit to the amount of dialogue nodes however if the writer wants a different initial dialogue in certain conditions, such as completing a quest given different initial dialogue, more code would need to be written.
3. The Regenerate Nodes button tells Unity to check through what nodes are present and that the user can access. This is needed as Unity doesn't check constantly what nodes should and shouldn't be present.

## W5
### Activity 1
1. While the horse is in the isMoving state, translate the horse to the right and rotate it back and forth
- Put an update node and connect a translate node to it
- Multiply the horse’s position by an object variable that determines its speed and multiply the product by Time.deltaTime and connect the product to the translate node.
- Test to see if it’s working correctly and unhook the translate node from update
- Make the horse rotate in one direction and test to find a good rotation speed
- At a certain point, make the horse switch rotating in the opposite direction and do it again for the other side
2. Stop the horse at a certain point and spawn in the horse’s ID and food card
- Add a game object at the desired stopping location
- Check if the horse has reached or passed the game object and transition to the idle state 
- Instantiate the horse’s ID and food card
3. After the player presses the accept or deny button, delete the horse’s IDs and food card and translate the horse left or right depending on the button pressed.
- When the player presses either button, fire a custom event in a transition graph
- Destroy the horse’s ID and food card game objects
- If the accept button was pressed, have the horse move to the right
- If the deny button is pressed, have the horse move to the left
- After the horse has reached a certain point, spawn in a new horse


### Activity 2
Since I somehow overlooked that the milestone 1 required us to make a functional state machine, I decided to finish the state machine during this class. During this class, I managed to get the horses to go the correct way after pressing one of the buttons, have a new horse enter after the previous one left, and semi animate the horses walking in.
