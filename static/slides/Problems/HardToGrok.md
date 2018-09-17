## When Code is Hard to Grok
Use declarative coding to improve code consistency.
```
foreach(stuff as item){
    push(details, getDetails(item));
}
```
```
details = stuff.map(item, {
    return getDetails(item);
})
```
