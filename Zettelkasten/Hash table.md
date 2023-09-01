*Data structure that stores unordered elements by mapping each element to a location in an array.*

Using an array and a hash function you pass a key into it to decide the location the element will be stored

tableArray[];
string key = name;
int value = 24;

Hash(key){
	tableArray[index] = value;
}

Solving collisions through chaining
if someone has the same index then we chain those values, basically storing multiple elements within a single array index.


