# searchahead v1.0.1
simple bootstrap-only replacement for typeahead solely.

### Fiddle
Feel Free to Fiddle: https://jsfiddle.net/howzitcal/euaogw12/

### Implementation
```html
<div class="form-group">
  <label for="findUser">Search Users</label>
  <input type="text" class="form-control" placeholder="eg. howzitcal" name="findUser" id="findUser">
</div>
```

```javascript
document.addEventListener("DOMContentLoaded", function(){
  new searchahead('#findUser', {
    // local: ["User 1", "User 2", "User 3", "User 4"],
    remote: "/api/find/user?user=%TERM",
    limit: 5,
    minLength: 2
  });
});
```
### Screenshots
![ScreenShot 2](https://i.imgur.com/7gQaMH5.png)

![ScreenShot 1](https://i.imgur.com/hAL1Hv5.png?1)

### Changelog
* V1.0.1 - Fixed miner issue where the click function doesn't work in the drop down due to a element focus issue
