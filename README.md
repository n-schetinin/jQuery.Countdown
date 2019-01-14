# jQuery.Countdown

            <h2>jQuery.Countdown plugin examples</h2>
            jQuery.Countdown is a simple plugin for countdown seconds from any time to 0. <br>
            Current time shows as "minutes":"seconds".<br>            
            <hr>
            <h3>Basic usage</h3>
            For basic usage you need to set start time in seconds.<br>
            Countdown automaticaly starts after initialization.<br>                        
            <pre>
$("#countdown").countdown({"seconds": 10}); </pre>
                        
            <h3>Ongoing parameter and control buttons</h3>
            Sometimes you may need to manual start/stop countdown. For this purpose you can use <code>"ongoing"</code> parameter.<br>
            Setting it to <code>false</code> disable automatic countdown start after init.<br>
            For manual start or stop the timer you need to add elements (buttons for example) on you page and specify their selectors in
            <code>"selector-start"</code> and <code>"selector-pause"</code> parameters.
            <pre>
$("#countdown").countdown({
    "seconds": 30,
    "ongoing": false,
    "selector-start":".countdown-start",
    "selector-pause":".countdown-pause"
}); </pre>
            
            
            <h3>Special classes and warning time</h3>
            You may want to add css classes to you countdown element depend of time left (for coloring for example).<br>
            You can do it by using the following parameters:<br>
            <code>"normal-class"</code> - until you reach zero<br>
            <code>"stop-class"</code> - when time's up<br>
            Also you can use <code>"warning-time"</code> with <code>"warning-class"</code> parameters to make an alert on little time left.<br>
            WARNING: use class names, not selectors!<br>
            <pre>
$("#countdown").countdown({
    "seconds": 10,
    "warning-time": 5,    
    "normal-class":"countdown-normal",
    "warning-class":"countdown-warning",
    "stop-class":"countdown-stop"    
}); </pre>
            
            <h3>Additional text</h3>
            Use <code>"prefix-text"</code> parameter to specify text before counting time. By default - empty string<br>
            <code>"stop-text"</code> is for text, when time is up. Default is "00:00".
            <br>
            <pre>
$("#countdown").countdown({
    "seconds": 5,    
    "prefix-text":"Time left: ",
    "stop-text":"Time's up!"    
}); </pre>
            
