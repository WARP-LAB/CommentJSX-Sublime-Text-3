# JSX (React) {/* comment */} macro and key shortcut for Sublime Text 3

---

### Setup
* Open `Preferences > Browse Packages`  
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
      }
``` 

