!DOCTYPE html>
<html>
    <head>
        <script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
         <meta charset="utf-8">
  <title>A-Frame with Countdown and Background Music</title>
  <meta name="viewport" content="width=device-width, initial-scale=1"><style>
      body { margin: 0; overflow: hidden; }

 #start-button {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        padding: 1em 2em;
        font-size: 1.5em;
        background: #222;
        color: white;
        border: none;
        cursor: pointer;
        z-index: 10;
      }

 #countdown {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 8em;
        font-weight: bold;
        color: white;
        display: none;
        z-index: 9;
        text-shadow: 4px 4px 10px rgba(0,0,0,0.7);
      }
    </style>

</head>
    <body> 
    <!-- Audio element -->
    <audio id="bg-music" loop>
      <source src="INSERT SOURCE PATH" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
 <!-- UI elements -->
    <button id="start-button">Start Experience</button>
    <div id="countdown">3</div>
        <a-scene>
            <!-- Set the background -->
            <a-sky color="lightblue"></a-sky>   
            <!-- Set the floor -->
            <a-plane position="0 0 0" height="100" 
                    width="100" rotation="-90 0 0"
                    color="black">
            </a-plane>
            
            <!-- Animated box that slides along the floor, once -->
            <a-box position="-8 1.5 -10" color="blue"
                    height="3" width="3" depth="1"
                    animation__1="
                    property: position;
                    from: -8 1.5 -10;
                    to: 8 1.5 -10;
                         dur: 2000;
                    
                                    loop: false

                    "
                     animation__2="
                     property: rotation;
                from: 0 0 0;
                to: 0 360 0;
                dur: 2000;
                loop: true
                    "
                       animation__3="
                property:scale;
                from: 0 1 -5;
                to: 0 0 0;
                     startEvents: click;     "
           
            ></a-box>
             <a-sphere
                color="yellow" position="0 1 -5" radius="1"
                animation="
                    property: color;
                    from: rgb(255,0,0);
                    to: rgb(0, 0, 150);
                    startEvents: click;
                     loop: true
                "
                
                animation__2="
                property:scale;
                from: 0 1 -5;
                to: 0 0 0;
                                    startEvents: click;         
                                     
                "
                >
                 
                 
            </a-sphere>
                        <a-camera>
                <a-cursor></a-cursor>
            </a-camera>
                    </a-scene>
                    

    </body>
</html>
