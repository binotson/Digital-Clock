# Digital-Clock
## Digital Clock with Date and Day
#### Visit the app by clicking this [Modern Clock](https://moderndigitalclock.netlify.app/)
![](gif/dc.gif)

#### Feel free to change or customize as much as you want
#### It sound awesome if you have a much better ideas to improve this
#### Do contribute and share your ideas with all other developers so that they can take advantage of your customization

Languages
================
- HTML
- CSS
- JavaScript

Base Design and Styling
================
In `index.html` you can get the base design of the clock

For styling i have used Bootstrap and custom styling you can get the CSS code from `style.css` file

JavaScript Code
================

In `clock.js` file you can get the Javascript code
`clock.js` have 3 main sections

- `tick()` function
- `getDayName()` fucntion
- `setInterval()` method

#### `tick()` fucntion :

```js
const tick = () =>{
    const current = new Date();
    
    let ss =current.getSeconds();
    let mm = current.getMinutes()
    let hh = current.getHours();
    let meridiem = 'AM';
    let currentDay = current.getDay();

    if(hh === 00){
        hh = 12
        meridiem = 'AM';
    }
    else if( hh === 12 ){
        meridiem = 'PM';
    }
    else if( hh > 12){
        hh = hh - 12
        meridiem = 'PM';
    }

    hours.textContent = `${hh<10? `0${hh}`:hh}`;
    minutes.textContent =`${mm<10? `0${mm}`:mm}`;
    seconds.textContent =`${ss<10? `0${ss}`:ss}`
    checkMeridiem.textContent = meridiem;
    date.textContent = current.toLocaleDateString();
    day.textContent = getDayName(currentDay);
    
}

```

