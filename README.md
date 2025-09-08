<!DOCTYPE html>
<html>
    <head>
        <script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
    </head>
    <body>
        <a-scene>
        <a-box
            position="0 1 -5"
            depth="2"
            height="2"
            width="2"
            color="tomato"
            animation="
                property: rotation;
                from: 0 0 0;
                to: 0 360 0;
                dur: 2000;
                easing: linear;
                loop: true;
            "
            
            animation__2="
            property: position;
            from: 0 1 -5;
            to: 3 1 -5;
            
            color="tomato">
            ">
        </a-box>
        </a-scene>
    </body>
</html>
