## Help, My Code is Breaking
Use Immutable Data to eliminate code fragility.
```
class Thing{
    constructor(id, stuff){
        this.id = id;
        this.stuff = Object.freeze(stuff)
    }
}
```
```
thing1 = new Thing(1, ['One','Two']);
thing1.stuff = ['Three', 'Four']; //Error
```
```
thing1N = new Thing(thing1.id, append(thing1.stuff, 'Three'));
```
