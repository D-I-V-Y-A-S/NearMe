# Ex04 Places Around Me
## Date: 05:04:2024

## AIM
To develop a website to display details about the places around my house.

## DESIGN STEPS

### STEP 1
Create a Django admin interface.

### STEP 2
Download your city map from Google.

### STEP 3
Using ```<map>``` tag name the map.

### STEP 4
Create clickable regions in the image using ```<area>``` tag.

### STEP 5
Write HTML programs for all the regions identified.

### STEP 6
Execute the programs and publish them.

## CODE

## index.html
```
<!DOCTYPE html>
<html lang="en">

<head>
    {% load static %}
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            margin: 0;
        }
    </style>
</head>

<body>
    <img src="{%static 'images/map.png' %}" width="800px" usemap="#map" onmousemove="coordinate(event)">
    <map name="map">
        <area shape="rect" coords="424,206,452,226" href="https://madrascoffeehouse.com/" title="MADRAS COFFEE HOUSE">
        <area shape="rect" coords="488,324,512,340" href="https://www.coffeeshastra.com/" title="COFFEE SHASTRA">
        <area shape="rect" coords="428,327,451,347" href="https://coffeeculture.co.in/" title="COFFEE CULTURE">
        <area shape="rect" coords="626,347,650,366" href="https://www.starbucks.in/dashboard" title="STARBUCKS">
        <area shape="rect" coords="368,24,396,42" href="https://www.agscinemas.com/" title="AGS CINEMAS">
    </map>
    <br>
    x-coordinate <input type="text" id="x"><br><br>
    y-coordinate <input type="text" id="y"><br>

    <script>
        function coordinate(event) {
            let x = event.clientX;
            let y = event.clientY;
            document.getElementById("x").value = x;
            document.getElementById("y").value = y;
        }
    </script>
</body>

</html>
```
## OUTPUT
![alt text](<map/Screenshot (454).png>)
![alt text](<map/Screenshot (455).png>)
![alt text](<map/Screenshot (456).png>)
![alt text](<map/Screenshot (458).png>)
![alt text](<map/Screenshot (457).png>)


## RESULT
The program for implementing image maps using HTML is executed successfully.
