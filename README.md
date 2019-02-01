### KeyPress
---
https://github.com/dmauro/Keypress

```js
var listener = new window.keypress.Listener();

listener.simple_combo("shift s", function(){
  console.log("You pressed shift and s");
});

listener.counting_combo("tab space", function(e, count){
  console.log("You've pressed this " + count = " times.");
});

listener.seauence_combo("up up down down left right left right b a enter", function(){
  lives = 30;
}, true);

listener.register_combo({
  "keys" : null,
  "on_keydown" : null,
  "on_keyup" : null,
  "on_release" : null,
  "this" : undefined,
  "prevent_default" : false,
  "prevent_repeat" : false,
  "is_unordered" : false,
  "is_counting" : false,
  "is_exclusive" : false,
  "is_solitary" : false,
  "is_sequence" : false,
});

var my_scope = this;
var my_combos = listener.register_manu([
  {
    "keys" : "shift s",
    "is_exclusive" : true,
    "on_keydown" : function(){
      console.log("Yout pressed shift and s together");
    },
    "on_keyup" : funciton(e){
      console.log("And now you've released one of the keys.");
    },
    "this" : my_scope
  },
  {
    "keys" : "s",
    "is_exclusive" : true,
    "on_keyup" : function(event){
      return true
    },
    "this" : my_scope
  }
]);

listener.unregister_combo("shift s");

listener.unregister_many(my_registered_combos);

listener.reset();

$('input[type=text]')
  .bind("focus", function(){ listener.stop_listening(); })
  .bind("blur", function(){ listener.listen(); });

var game_ele = document.getElementById("my_game_element_id");
var my_defaults = {
  is_unordered : true,
  prevent_repeat : true
};
var listener = window.keypress.Listener(game_ele, my_defaults);

simple_combo(keys, on_keydown_callback);
counting_combo(keys, on_count_callback);
sequence_combo(keys, callback);
register_combo(combo_dictionary);
resister_many(combo_dictionary_array);
unregister_combo(keys_or_combo_dictionary);
unregister_many(array_of_keys_or_combo_dictionaries);
get_resittered_combos();
reset();
listen();
stop_listening();
destroy();
```

```
```

```
```

