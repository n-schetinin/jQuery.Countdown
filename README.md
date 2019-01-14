<h1>jQuery.Countdown</h1>

jQuery.Countdown is a simple plugin for countdown seconds from any time to 0. <br>
Current time shows as "minutes":"seconds".

<h2>Basic usage</h2>

For basic usage you need to set start time in seconds.<br>
Countdown automaticaly starts after initialization.<br>                        
```
$("#countdown").countdown({"seconds": 10});
```                        

<h2>Ongoing parameter and control buttons</h2>

Sometimes you may need to manual start/stop countdown. For this purpose you can use **"ongoing"** parameter.<br>
Setting it to false disable automatic countdown start after init.<br>
For manual start or stop the timer you need to add elements (buttons for example) on you page and specify their selectors in
**"selector-start"** and **"selector-pause"** parameters.<br>
```
$("#countdown").countdown({
    "seconds": 30,
    "ongoing": false,
    "selector-start":".countdown-start",
    "selector-pause":".countdown-pause"
});
```
            
<h2>Special classes and warning time</h2>

You may want to add css classes to you countdown element depend of time left (for coloring for example).<br>
You can do it by using the following parameters:<br>
**"normal-class"** - until you reach zero<br>
**"stop-class"** - when time's up<br>
Also you can use **"warning-time"** with **"warning-class"** parameters to make an alert on little time left.<br>
**WARNING:** use class names, not selectors!<br>
```
$("#countdown").countdown({
    "seconds": 10,
    "warning-time": 5,    
    "normal-class":"countdown-normal",
    "warning-class":"countdown-warning",
    "stop-class":"countdown-stop"    
}); 
```

<h2>Additional text</h2>

Use **"prefix-text"** parameter to specify text before counting time. By default - empty string<br>
**"stop-text"** is for text, when time is up. Default is "00:00".<br>
```            
$("#countdown").countdown({
    "seconds": 5,    
    "prefix-text":"Time left: ",
    "stop-text":"Time's up!"    
});
```
            
