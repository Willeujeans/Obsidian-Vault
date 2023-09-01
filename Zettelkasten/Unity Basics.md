Game objects are made from components
## Public objects
*allows you to drop an object into the UI interface*
public GameObject variableName
## GetComponent
*grabs the sprite renderer component on the script's parent gameObject*
myRenderer = GetComponent$<$SpriteRenderer$>$();
## Instantiate
*creates a game object*
Instantiate(gameObject, position, rotation);
Instantiate(manGuy, Vector3.zero, Quaternion.Identity);
//Quaternion.Identity, means no rotation

## Destroy
*removes a game object*
Destroy(gameObject, lifeTime);

## Handling Arrow Inputs
*returns 1 for held, 0 for not held*
Input.GetAxisRaw("Vertical");
Input.GetAxisRaw("Horizontal");

## Basic 2D Movement
private void Update(){
Vector3 playerInput = new Vector3(Input.GetAxisRaw("Horizontal"), Input.GetAxisRaw("Vertical"),0);

transform.position = transform.position + playerInput.normalized * speed * Time.deltaTime;
}
we are using a vector 3 because Unity is a 3D engine, z will remain 0.
The x and y will be affected by the movement keys, 0 or 1
we then increment the transform.position by itself plus the normalized version of the input, making it so the input remains capped. Multiply it by the speed we want. Multiply it by deltaTime so that its frame rate independent.

## MoveTowards
*moves a gameObject towards the targets position*
Vector2.MoveTowards(startPosition, target, speed);

## Triggers
private void OnTriggerEnter2D(Collider2D other){
 if(other.tag == "tagName"){
  //code to execute
 }
}