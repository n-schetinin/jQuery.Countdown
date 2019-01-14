# jQuery.Countdown
# Plugin for countdown from specified time to zero
# jQuery.Countdown is a simple plugin for countdown seconds from any time to 0.
# Current time shows as "minutes":"seconds".

1. Basic usage
For basic usage you need to set start time in seconds.
Countdown automaticaly starts after initialization.                        
            
$("#countdown").countdown({"seconds": 10});
            
2. Ongoing parameter and control buttons

Sometimes you may need to manual start/stop countdown. For this purpose you can use "ongoing" parameter.
Setting it to false disable automatic countdown start after init.
For manual start or stop the timer you need to add elements (buttons for example) on you page and specify their selectors in
"selector-start" and "selector-pause" parameters.
            
$("#countdown").countdown({
    "seconds": 30,
    "ongoing": false,
    "selector-start":".countdown-start",
    "selector-pause":".countdown-pause"
});

3. Special classes and warning time
            
You may want to add css classes to you countdown element depend of time left (for coloring for example).
You can do it by using the following parameters:
"normal-class" - until you reach zero
"stop-class" - when time's up
Also you can use "warning-time" with "warning-class" parameters to make an alert on little time left.
WARNING: use class names, not selectors!
            
$("#countdown").countdown({
    "seconds": 10,
    "warning-time": 5,    
    "normal-class":"countdown-normal",
    "warning-class":"countdown-warning",
    "stop-class":"countdown-stop"    
}); 
    
4. Additional text

Use "prefix-text" parameter to specify text before counting time. By default - empty string
"stop-text" is for text, when time is up. Default is "00:00".
            
$("#countdown").countdown({
    "seconds": 5,    
    "prefix-text":"Time left: ",
    "stop-text":"Time's up!"    
}); 
