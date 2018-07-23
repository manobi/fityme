# FITYME

> FITYME stands for **"Fake it til you make it"**

A Stylus library to generate skeleton screens, through svg placeholder as data URI background in order to help you improve the perceived loading time of your apps.

----

## Usage
```bash
npm install --save-dev fityme
```

```stylus
@require './node_modules/fityme/index.styl'

body
    background #eee url(
        fityme(318, 198, 
            rect(100%, 100%, 0, 8, #ffffff), 
            rect(`200, 120, center, 16, #ccc),
            rect(270, 16, center, 148, #eee), 
            rect(220, 16, center, 168, #eee)
        )
    );
```

**GENERATES**

<svg xmlns='http://www.w3.org/2000/svg' width='318' height='198'>
    <rect rx='0' ry='0' fill='#fff' x='0' y='8' width='100%' height='100%' transform='translate(0, 0)' /> 
    <rect rx='0' ry='0' fill='#ccc' x='50%' y='16' width='200' height='120' transform='translate(-100, 0)' /> 
    <rect rx='0' ry='0' fill='#eee' x='50%' y='148' width='270' height='16' transform='translate(-135, 0)' /> 
    <rect rx='0' ry='0' fill='#eee' x='50%' y='168' width='220' height='16' transform='translate(-110, 0)' />
</svg>

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

## ft-xs-x
For extra small screens, define the number of times a card can be repeated.

## ft-sm-x
For small screens, define the number of times a card can be repeated.

## ft-md-x
For medium sizes screens, define the number of times a card can be repeated.

## ft-lg-x
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