##Running  and visiting the website

Prerequisites:

Python (e.g. Python-2.7.12) installed


### Getting started

1. Run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

2. Open a browser and visit localhost:8080

##List of optimizations

###Optimizations for PageSpeed Score

1. pizzeria.jpg was replaced with compressed thumbnail; profilepic.jpg was compressed
2. Google analytics js loading is shifted to the end of html body
3. media="print" attribute for print.css
4. Web fonts usage removed
5. Styles.css was minified and inserted directly into index.html

###Getting rid of Jank

1. Move phase calculaton out of the loop to avoid jank from scrolling
2. Debounce drawing on scrolling
3. Calculation of new pizza size after slider position change was taken out of the loop
4. Removal of DOM requests (e.g. document.getElementById()) from loops
5. Calculation of the number of pizzas visible in the background (instead of fixed 200)