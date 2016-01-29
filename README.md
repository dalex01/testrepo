
Project 4:  Website Optimization
Resubmit Date:  08/14/2015
Name:  Kay Lee (kayklee2014@gmail.com)

Work Summary:  The content of the given website has been modified to meet the following web performance objectives.   


Objective 1:  The PageSpeed score of 90 is for index.html (both Mobile and Desktop scores should be at least 90).

	Modified index.hml to obtain the PageSpeed score of 90 or higher as followings: 
	a. load the google font asynchronously by using JavaScripts
	b. specify media query for loading css/print.css in order to remove an unnecessary rendering block 
	c. remove loading css/style.css and replace it with inline css codes   
	d. load an external javaScripts, http://www.google-analytics.com/analytics.js, asynchronously with adding async
	e. load smaller img/profilepic.jpg, which is resized from 15KB to 2KB

	How to Test in Winodws 7:
	a. set up a local server using python
	b. run python from the project folder by doing the following
	   C> cd C:\project4
	   C> python -m SimpleHTTPServer 8080
	c. run ngrok to make the local server accessbile remotely
	   C> ngrok http 8080
	d. copy the forwarding address given by ngrok
	e. open the PageSpeed Insights page and paste the forwarding URL into the analyze input box
	f. press the Analyze button
	g. review the scores and recommendations 

	Test Results:  The PageSpeed shows the scores of 93 and 96 for the Mobile and Desktop scores respectively.   


Objective 2:  The frame rate of 60fps should be obtained for the pizza.html page (views/pizza.html).

	Modified views/main.js to obtain the frame rate of 60 fps for the pizza.html page as following:
	a. move variables, pizzasDiv and elem, to outside of the for loop to avoid redundant calculations
	b. replace document.querySelectorAll() with getElementsByClassName()
	c. create new local variables in updatePositions to hold static values in order to avoid redundant calculations  
	d. simplify computations by replacing redundant calculations with computed static values in the for loop
	e. reduce loading the sliding pizza pictures from 200 to an optimal value by calculation
	f. load smaller img/pizzeria.jpg, which is resized from 2.3MB to 26KB
	g. define a loop threshold value at the loop initialization
	h. Move render blocking external css to the html header

	How to Test in Windows 7:
	a. open http://78c9fc19.ngrok.io/views/pizza.html (an example of ngrok forwarding addresses) with the Chrome browser
	b. open the Chrome developer tools
	c. press the Timeline tab 
	d. start recording by pressing record icon
	e. scroll down the web page for 3 to 4 seconds
	f. stop recording
	g. evaluate the results shown in the timeline

	Test Results: It sporadically shows a couple of lower than 60fps bars in the Timeline but mostly loads 60fps or higher number of fps.  


Objective 3:  The time to resize pizzas is less than 5 ms.

	Modified the function, changePizzaSizes, to efficiently calculate the new pizza size as following:
	a. move and calculate static local variables outside of the for loop to avoid redundant calculations

	How to Test in Windows 7:
	a. open http://78c9fc19.ngrok.io/views/pizza.html (an example of ngrok forwarding addresses) with the Chrome browser
	b. open the Chrome developer tools
	c. press the Console tab
	d. use the slider on the pizza.html to change pizza sizes
	f. check the time to resize pizzas logged on the Console 

	Test Results:  It takes on average less than 2 ms to resize pizzas.  



References

https://developers.google.com/web/fundamentals/performance/critical-rendering-path/

https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css?hl=en

https://developers.google.com/web/fundamentals/performance/critical-rendering-path/page-speed-rules-and-recommendations?hl=en

https://discussions.udacity.com/t/optimize-css-delivery-of-google-font/15573

https://github.com/udacity/fend-office-hours/tree/master/Web%20Optimization/Effective%20Optimizations%20for%2060%20FPS

https://ngrok.com/faq

https://developers.google.com/speed/pagespeed/

https://developer.chrome.com/devtools/docs/tips-and-tricks

https://developer.mozilla.org/en-US/docs/Web/API/Screen/height

http://www.w3schools.com/jsref/prop_screen_height.asp

https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById

https://robots.thoughtbot.com/how-to-write-a-great-readme





