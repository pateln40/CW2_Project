# CW2_Project Learning Journal 


13/03/21


Created my first package for a player movement, watched a few tutorials to get a better undertstanding of what I needed to do for my script. For this pplayer movment script I decided to use a PlayerController component to make sure the player moves according to the environment (the colliders). The reason behind the Character Controller is that it provides basic collider responses without any physics. A simple script but I made small mistakes such as spelling 'characterController' wrong in this section of this script and forgetting to add the CharacterController component to the player object in the inspector.



        if (characterController.isGrounded && Input.GetButton("Jump"))
            moveVector.y = jumpSpeed;

        moveVector.y -= gravity * Time.deltaTime;

        characterController.Move(moveVector * Time.deltaTime);
    }


18/03/21

Attempted to make a script that teleports an object to the mouse position, but the object didn't move at all in the scene. Spent hours trying to figure out why but I gave up and took a break from this problem.

            using System.Collections;
            using System.Collections.Generic;
            using UnityEngine;
 
              public class Mouse : MonoBehaviour
           {
 
             public GameObject MousePosGameObject;
 
             Vector3 worldPosition;
 
          void Update()
    {
           Vector3 mousePos = Input.mousePosition;
           mousePos.z = Camera.main.nearClipPlane;
            worldPosition = Camera.main.ScreenToWorldPoint(mousePos);
 
        MousePosGameObject.transform.position = new Vector2(worldPosition.x, worldPosition.y);
       }
  
    }
  

19/03/21

     using UnityEngine;
 
        public class Mouse : MonoBehaviour
    {
       public GameObject MousePosGameObject;
 
       void Update()
       {
         Vector3 mousePos = Input.mousePosition;
         mousePos.z = MousePosGameObject.transform.position.z - 
         Camera.main.transform.position.z ;
 
          MousePosGameObject.transform.position = Camera.main.ScreenToWorldPoint(mousePos);
       }
    }


23/02/21

I attemped to make AI for my third package this involved using the NevMeshAgent and Baking function . This allows the AI to move around the map that is walkable, and the walls that isn't walkable. Since I've made AI it wasn't too bad to make but again I bumped into silly errors due to spelling or missing words. In this line of code I orginally wrote 'NavMesh' instead if 'NavMeshAgent'.

    {
        Mob = GetComponent<NavMeshAgent>();
    }












