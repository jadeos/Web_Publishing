For this assignment, I designed and implemented a theme for Tate gallery using three important features. 
## Homepage
The homepage is the index.jade template. It consists of a carousel with 10 populated images from the database and two high charts displaying data about 10 artists form the database. The reason I limited the results to 10 is because of the time it takes to load. This can easily be changed in the index.js routes file when the data is being queried. 
## Charts
###### The total of artists born in a given year
This is a basic line chart.  I had to write a script that found each year and each artist. I had a counter variable set to 1, since at least one artist would be born in that year. If more than one artist was born that year, the counter would add 1 for each of those artists. 
 
###### The percentage of total works sold by each artist.
The chart below shows the percentage of the total works sold by each artist. Currently I’ve limited it to 10 artists as it was faster to load. This can be easily modified in the index.js routes file. I’ve decided to do this chart as I thought it had some value. For example, users  might want to have a clear view of the artist data.  The user can also view more information by clicking on the pie section of the image and the artist page will load, displaying that specific artist’s details such as birth year etc.  The navigation part I had to add a click event and an anchor tag in my artist.jade file with a div id of the artist name. This made it easy for me to navigate to a section of the page containing the artist’s information. 
 

## Carousel
I’ve also added a carousel on the home page as I wanted to give users a gallery-like feel for the application. I could have done an image gallery, however, I felt like the carousel was more suitable for what I had originally planned for the application. The carousel shows the user the artwork image, and the artist. Users can view more information about that artwork by clicking on the image. Then the artworks.jade file will display the current artwork in the artwork directory. The carousel was achieved using bootstrap and my own customised JavaScript. The JavaScript part was used to access loop through each result and display them in the carousel.
 
## Artists.jade 
In this page, users can view a list of the artists in Tate gallery. It is currently limited to 10 as it is faster to load. In this file, the user can see the artist name, date of birth, gender, total works and url. However, this data can be modified to add more data about the artist. 
 
## Artworks.jade
In this page, users can view a list of the artworks in the tate gallery. It is currently limited to 10 as it is faster to load. In this file, the user can see the artwork title, acquisition year, Url, medium and dimensions. However, this data can be modified to allow more data about the artist to be added or changed.
  

## Settings.jade
This file is responsible for changing the theme of the data. 
###### Theme Changes
I designed two different themes for the application that can be easily adjusted by modifying the css. 
•	Default theme: 
o	This is the original theme that had been designed. I’ve chosen a more neutral theme as it is more readable. The styling of this can be adjusted or changed by a developer if needed. 
•	Ocean theme: 
o	This is more of a personalised theme. The styling is currently set to change the background colour to an image of an ocean. This wasn’t the ideal outcome however I wanted to demonstrate the concept by getting something working.  I would like to do more with this if I had more time to do so. 
I created the two themes and made them persistent to the database by storing a value in the database called ‘theme’. If theme was set to ‘default’, the default jade templates would load (artists.jade, artworks.jade). These templates would have their own personalised styling in the CSS. When the ocean theme is selected, the ‘theme’ value will update to be called ‘ocean’ and when the user loads either the artist or artworks pages, the ocean theme style would be displayed using separate jade files (art.jade, gallery.jade). 

I had only enough time to change the overall theme for both artists.jade and artworks.jade. The reason I didn’t change the theme for settings or the homepage is because I had difficulty changing the entire thing, including the nav menu which is in layout.jade. 




 

 
## Design 
For parts of my design I used some bootstrap features. In the artist and artworks pages, I have styled it using bootstrap and customised it with my own css by changing the colours etc. I also used bootstrap for the carousel however, I found it challenging to retrieve the images from the database. This took some time to figure out the logic behind it and implement it using Jade. 
The charts were created using theHighcharts.js API. This was interesting to implement as it meant that I had to research ways to make the charts more dynamic and readable.  
## Conclusion and future works
This assignment was an interesting one to do. I enjoyed specifically learning about high charts work. For future work, I would like to achieve many elements that I couldn’t achieve due to time restrictions. For example, I’d like to get the line chart to show the year the artist was born and the artist instead of the number. I would like to change the settings page so that the user can change other css elements such as font style, text colour, navigation menu etc. I would also re-style the ocean theme completely. 
Since these are only minor changes that I would make, I am quite satisfied with this project as it demonstrates the main concepts that I wanted to achieve. 

