# keyboard-tones

Simple npm module that maps the 12 musical tones to the keyboard

    npm install --save keyboard-tones

## Usage: 

    var kt = require('keyboard-tones');
    console.log(kt);

## The mapping: See [index.js](index.js)

On the keyboard, the 12 tones are found here: 

    a
     w
    s
     e
    d 
    f
     t
    g
     y
    h
     u
    j

## Example
~~~php
        document.addEventListener("keydown", function (e){
            var k = e.key;
            if (k in keyboardTones) {
                // Octave = 3
                let note = keyboardTones[k] + '3';
                parseNoteon(note);
            }
        });
        
        document.addEventListener("keyup", function (e){
            var k = e.key;
            let note = keyboardTones[k] + '3';
            parseNoteoff(note);
        });
~~~
## License

MIT © Dennis Iversen
