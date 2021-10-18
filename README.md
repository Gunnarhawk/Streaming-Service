# Streaming-Service

This code is uploaded on codepen.io, visit this link to view it live -> https://codepen.io/Gunnarhawk/pen/vYJEwoM

My goal for this project was to make the UI of a streaming service and have it be scalable/responsive on mobile. 

The movie cards are retrieved from an object array in js. This object array can be changed out for an http request that returns the same data structure, but in this application, the data is hard coded in inside of the global variable 'cards'

A large part of that was getting the cards to fit on the screen and have their background scale with their size, I then wrote an equation to do this:

let scale = (100 * ((carousel_width - btn_width) / num_cards - card_margin * 2)) / initial_width;

carousel_width is the width of the whole carousel without margin or padding
btn_width is the width of both of the side buttons
num_cards is the number of cards i want to display on the screen, this value is changed based on the size of the user's screen
card_margin is the margin (spaces) between the cards
initial_width is the initial width (in px) of the background image (1920 from 1920x1080)

This equation then gives a scale % that I could multiply the width and height of the card by to keep the aspect ratio of the image the same and have it fit well inside of the card
