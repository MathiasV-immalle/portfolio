# HTML
## Part 3: Web storage objects + Geolocation
## Web storage objects
- sessionStorage

`sessionStorage()`

Session Storage is destroyed once the user closes the browser.

- localStorage

`localStorage()`

Local Storage stores data with no expiration date.

Storing a Value:	    `localStorage.setItem("key1", "value1");`

Getting a Value:      `alert(localStorage.getItem("key1"));`

Removing a Value:	    `localStorage.removeItem("key1");`

Removing All Values:	`localStorage.clear();`

## Geolocation
```
navigator.geolocation.getCurrentPosition();
```
Gets the location of the user.

### You still want to learn more? Feel free to visit Part 4 [HERE](Scalable-vector-graphics.md)
