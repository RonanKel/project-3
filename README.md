Editor=Ronan Kelly
DateLastModified=02/7/23
Description:

	As far as implementation went I started by modifying the DOCKERFILE and copying credentials.ini into /vocab. From there I went into and cahnged flask_vocab.py and vocab.html.
The way I implemented was I took the large if statement in the flask_vocab.py check() function and made it check the same things but then set rslt to be a dictionary with the key cond_status and the
value to be whatever is right for the situation (I chose a different value for each occation so I could read the case in the .html file). Then I just returned a jsnoify() with the result being the rslt
dictionary.
	In the .html file I delted everything that had to do with JINJA and then made sure that there would be no way to submit the text box, by pressing enter or the submit button (I deleted the submit button). Then I replaced it with my own function that I got from minijax.html. It already had everything I need to read key presses. Then I passed any letter key press into my python file, which depending
on what the total string said, gave an output. I then wrote an if statement to handle all the different possible conditions. Then after I had as many letters as I needed, I redirected to the success page, which I found out how to do using stack overflow (https://stackoverflow.com/questions/503093/how-do-i-redirect-to-another-webpage). 
