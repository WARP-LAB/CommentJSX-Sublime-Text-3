# JSX (React) {/* comment */} macro and key shortcut for Sublime Text 3

---

### Setup
* Open `Preferences > Browse Packages`  
* Copy `CommentJSX.sublime-snippet`
* Copy `CommentJSX.sublime-macro`
* Open `Preferences > Key Bindings - User` and add shortcut as desired

```
    { 
      "keys": ["super+ctrl+/"],
      "command": "run_macro_file",
      "args":
        {
          "file": "Packages/User/CommentJSX.sublime-macro"
        },
      "context": 
        [
          {
            "key": "selector",
            "operator": "equal",
            "operand": "source.js,source.jsx"
          }
        ]
    },
    {
      "keys": ["super+alt+/"], 
      "command": "insert_snippet", 
      "args": { "name": "Packages/User/CommentJSX.sublime-snippet" },
      "context": 
        [
          {
            "key": "selector",
            "operator": "equal",
            "operand": "source.js,source.jsx"
          }
        ]
    }
``` 

### Notes

Probably one should use only `snippet` as it works both ways - inserts comment at cursor position, but if user has selected code, wraps it within JSX comment. `macro` only inserts empty comment at cursor position.
