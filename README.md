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
![Alt text](./demo/readme.svg)

* [Helper classes](#)
* [API](#)

> No matter what impossible situation you are dealing with, you might always **FITIMY**.

----------

## Helper classes

### ft-x
Define the number of times a card can be repeated based on a **8 columns grid**.
You can even combine some classes, to dictate how the cards will be rendered o different screen sizes.

To repeat the card created before (.ft-products) 3 times do the following:
```html
<ul class="ft-products ft-3"></ul>
```

If you want to change how many times the card will show on extra small screens:
```html
<ul class="ft-products ft-3 ft-xs-1"></ul>
```

All options available:

| Repeat-(n) | Extra Small Screen | Small screen | Medium screens | Large screens |   
| -----------| ------------------ |------------- |--------------- |-------------- |
| .ft-1      | .ft-xs-1           | .ft-sm-1     | .ft-md-1       | .ft-lg-1      |
| .ft-2      | .ft-xs-2           | .ft-sm-2     | .ft-md-2       | .ft-lg-2      |
| .ft-3      | .ft-xs-3           | .ft-sm-3     | .ft-md-3       | .ft-lg-3      |
| .ft-4      | .ft-xs-4           | .ft-sm-4     | .ft-md-4       | .ft-lg-4      |
| .ft-5      | .ft-xs-5           | .ft-sm-5     | .ft-md-5       | .ft-lg-5      |
| .ft-6      | .ft-xs-6           | .ft-sm-6     | .ft-md-6       | .ft-lg-6      |
| .ft-7      | .ft-xs-7           | .ft-sm-7     | .ft-md-7       | .ft-lg-7      |
| .ft-8      | .ft-xs-8           | .ft-sm-8     | .ft-md-8       | .ft-lg-8      |

### .ft-single
Restrict the the num of cards to only one.
```html
<!-- Only one card no matter what screen size --> 
<ul class="ft-products ft-single"></ul>
```

### .ft-single-row
Allow only a single row of cards.
```html
<ul class="ft-products ft-single-row"></ul>
```

### .ft-single-column
Allow only a single column of cards.
```html
<ul class="ft-products ft-ingle-column"></ul>
```

### .ft-full
Makes one only card to extend itself until it fit the entire block.
```html
<ul class="ft-products ft-full"></ul>
```

----------

## API

### fityme(x, y, content)
Generates the card canvas.
```stylus
fityme(318, 198, ...content)
```

### rect(wdth = 100%, hght = auto, x = 0, y = 0, fill = #ccc, radius = 0, anim = false)
Draw a rectangle
```stylus
rect(200, 120, center, 16, #ccc, 5, true),
```

### sqr(size, x, y)
Draw a square
```stylus
square(200, ...)
```
### crc(size, x, y)
Draw a circle
```stylus
circle(200, ...)
```


------

## Contribute
Please let me know of the bugs you find. 
Don't like Stylus? fell free to port it to your favorite stylesheet processing language, mas let me know so I can improve this project by learn from your proccess.