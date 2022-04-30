# Fabric-js-Zoom-in-zoom-out-project
<html>

<head>
    <title>Basic Animations Part 2 - scaling</title>
    <script type="text/javascript">
        var width = 500;
        var difference = 2;
        var interveralID = 0;

        function increase() {
            clearInterval(interveralID);
            interveralID = setInterval(expand, 10);
        }

        function decrease() {
            clearInterval(interveralID);
            interveralID = setInterval(shrink, 10);
        }

        function expand() {
            if (width < 700) {
                width = width + difference;
                document.getElementById("img1").style.width = width;
                console.log(width);
            } else {
                clearInterval(interveralID);
            }

        }

        function shrink() {
            if (width > 500) {
                width = width - difference;
                document.getElementById("img1").style.width = width;
                console.log(width);
            } else {
                clearInterval(interveralID);
            }

        }
    </script>
</head>

<body>

    <br>
    <br>
    <img onmouseover="increase()" onmouseout="decrease()" id="img1" src="download.jpg" width="700" />
</body>

</html>
