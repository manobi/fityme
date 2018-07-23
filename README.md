# FITYME

> FITYME stands for **"Fake it til you make it"**

A Stylus library to generate skeleton screens, through svg placeholder as data URI background in order to help you improve the perceived loading time of your apps.

----

## Usage
```bash
npm install --save-dev fityme
```

Require and draw your **card**.

```stylus
@require './node_modules/fityme/index.styl'

body
    background #eee url(
        fityme(318, 198, 
            rect(100%, 100%, 0, 8, #ffffff), 
            rect(200, 120, center, 16, #ccc, 5, true),
            rect(270, 16, center, 148, #eee), 
            rect(220, 16, center, 168, #eee)
        )
    );
```

Outputs:

```css
body {
  background: #eee url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='318' height='198'><defs><linearGradient id='shiny'><stop offset='0%' stop-color='white'></stop><stop offset='100%' stop-color='black'><animate attributeName='offset' from='0' to='1' dur='2.5s' repeatCount='indefinite' /></stop><stop offset='100%' stop-color='white'></stop></linearGradient><mask id='shining'><rect x='0' y='0' width='200%' height='100%' fill='url(#shiny)' /></mask></defs><rect rx='0' fill='#fff' x='0' y='8' transform='translate(0, 0)' width='100%' height='100%' /> <rect mask='url(#shining)' rx='5' fill='#ccc' x='50%' y='16' transform='translate(-100, 0)' width='200' height='120' /> <rect rx='0' fill='#eee' x='50%' y='148' transform='translate(-135, 0)' width='270' height='16' /> <rect rx='0' fill='#eee' x='50%' y='168' transform='translate(-110, 0)' width='220' height='16' /></svg>");
}
```

> No matter what impossible situation you are dealing with, you might always *FITIMY*

----------

## API

### fityme(x, y, content)
Generates the card canvas

### rect(width, height, x, y)
Draw a rectangle

### sqr(size, x, y)
Draw a square

### crc(size, x, y)
Draw a circle


## Helper classes

### ft-x
Define the number of times a card can be repeated.

### ft-xs-x
For extra small screens, define the number of times a card can be repeated.

### ft-sm-x
For small screens, define the number of times a card can be repeated.

### ft-md-x
For medium sizes screens, define the number of times a card can be repeated.

### ft-lg-x
Define the number of times a card can be repeated on large sizes screens.

### .ft-single
Restrict the the num of cards to only one.

### .ft-single-row
Allow only a single row of cards.

### .ft-single-column
Allow only a single column of cards.

### .ft-full
Makes one only card to extend itself until it fit the entire block.

------

## Contribute
Please let me know of the bugs you find. 
Don't like Stylus? fell free to port it to your favorite stylesheet processing language, mas let me know so I can improve this project by learn from your proccess.