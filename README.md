За основу взят [пример](https://codepen.io/jamesbarnett/pen/vlpkh) и не много упрощен.

### Структура HTML
```html
<div class="rating">
  <input type="radio" id="rating5" name="rating" value="5"><label for="rating5"></label>
  <input type="radio" id="rating4" name="rating" value="4"><label for="rating4"></label>
  <input type="radio" id="rating3" name="rating" value="3"><label for="rating3"></label>
  <input type="radio" id="rating2" name="rating" value="2"><label for="rating2"></label>
  <input type="radio" id="rating1" name="rating" value="1"><label for="rating1"></label>
</div>
```
### Стили
```css
.rating {
  display: flex;
  flex-direction: row-reverse;
  justify-content: flex-end;
}

.rating > input { 
  display: none; 
}

.rating > label {
  color: grey;
}

.rating > label:before {
  content: "\f005";
  display: block;
  font-family: FontAwesome;
  font-size: 1.25em;
}

.rating > input:checked ~ label {
  color: yellow;
}
```
