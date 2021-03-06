$.fn.serializeObject makes an object out of form elements inside of the specified item.

Example:

    <div id="test">
      <input name="text1" value="txt-one" />
      <input type="checkbox" name="top[child][]" value="1" checked="checked" />
      <input type="checkbox" name="top[child][]" value="2" checked="checked" />
      <input type="checkbox" name="top[child][]" value="3" checked="checked" />

      <select name="another[select]">
        <option value="opt"></option>
      </select>
    </div>


```javascript
$( '#test' ).serializeObject();
```

Returns

```javascript
{ text1: "txt-one",
  top: {
    child: [ "1", "2", "3" ]
  },
  another: {
    select: "opt"
  }
}
```
