## When Code is Hard To Test
Remove complexity to get to core logic.
```
async function logStuffToConsole(ids){
    url = '/getStuff?ids={join(',',ids)}'; //
    stuff = await fetchJSON(url); //
    foreach(stuff as item){
        details = 'Thing: {item.id}, created on {item.date}'; //
        console.log(details); //
    }
}
```
```
function getStuffDetails(stuff){
    details = [];
    foreach(stuff as item){
        push(details, getDetails(item));
    }
    return details;
}
```
