Link: (https://nishantb15.github.io/Roll-A-Ball-V2/)[]

My first cool new feature is a jail area (green and black jail-like structure) where the player needs to collect a green cube in order to open the green door. Inside the jail are Pickups needed to win the game. I made the cube and the door the same color so as to avoid confusion.

public GameObject keyWall;
void OnTriggerEnter(Collider other)
{
       if (other.gameObject.CompareTag("Key Square"))
       {
             other.gameObject.SetActive(false);
             keyWall.SetActive(false);
       }
}
I use the unity editor to assign my green wall to the keyWall game object as well as set the tag of the green Key Cube as "Key Square". In line 4 and 5, the Key Cube and Key Wall object are deactivated if the player collides with the Key Cube and the player is allowed to enter the jail room where he/she can obtain more points.

My second feature is a slide which the player can go up and down in order to access the jail area. I used the unity editor to create a cube object and then i changed the scale to form a cuboid. Then I rotated the cuboid approximately 45 degrees in the z-direction.

In order to ensure the players do not fly out of the playing arena when climbing up the slide, I increased the size of the walls from each side except the side from which you view the ball so the camera's field of view is not obstructed from the moving ball. I also changed the maximum score from 12 to 16 in order to ensure the player utilizes each cube (Pick ups (Yellow), Warp Cubes (Orange), Gate Key Cubes (Green) and Speed Ups (Blue)). If a player collides with a Stop Cube (Red), the game is over and a messaged is displayed on the screen.

