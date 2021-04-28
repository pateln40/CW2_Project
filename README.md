# CW2_Project Learning Journal 


13/03/21


Created my first package for a player movement, watched a few tutorials to get a better undertstanding of what I needed to do for my script. For this pplayer movment script I decided to use a PlayerController component to make sure the player moves according to the environment (the colliders). The reason behind the Character Controller is that it provides basic collider responses without any physics. A simple script but I made small mistakes such as spelling ''characterController'' wrong in this section of this script and forgetting to add the CharacterController component to the player object in the inspector.



        if (characterController.isGrounded && Input.GetButton("Jump"))
            moveVector.y = jumpSpeed;

        moveVector.y -= gravity * Time.deltaTime;

        characterController.Move(moveVector * Time.deltaTime);
    }




















I attemped to make AI for my game, this involved using the NevMeshAgent and Baking function . This allows the AI to move around the map that is walkable, and the walls that isn't walkable, since my game is in a maze the AI needs to move around the map without it bumping into the walls, I also made the AI to move at certain points as well so that it can move in a certain area rather than the whole map, since I plan to make more than one AI in my scene. I did have some issues with the waypoints, the AI wouldn't face in the right direction, but I just redid the waypoints and it worked.


