# 15112-Term-Project
#For my project I made the classic videogame Pong. When you open up the game,
#you are brought to the main menu page. While on this page, if you don't know how to play,
#you can click on the controls button to bring you to the controls page. This will clearly show
#you what the controls are depending on whether you are playing one player mode or two player mode.
#In addition to the controls page, there is also an option to click on the settings button
#on the main menu. If you do this, it will bring you to the settings page and allow you to configure the 
#settings to your liking. The default settings are normal difficulty and wrap around turned on. 
#In case you don't know what wrap around is, if it is turned on, while playing in either mode,
#if a paddle goes fully offscreen it will warp to the opposite site of the screen from 
#which it moved off of. If wrap around is turned off, both paddles in both modes will not be allowed 
#to move offscreen. There are three different difficulties in this game: easy, normal, and insane.
#If the game is beaten on insane mode, you will have the option to turn on switch up mode in setings.
#This makes the paddle white and the ball black. In one player and two player modes, each paddle is broken up
#into five different zones. Hitting the ball in a corner zone (the very top or very bottom 
#of the paddle shoots the ball with a faster velocity in addition to making the ball's y step
# more extreme. Hitting the ball in the upper or lower zone (the zones just below and above the top corner
#and bottom corner respectively, it will shoot the ball faster than if it hits the middle of the paddle,
#but slower than if it hits a corner. The ball's y-step is slightly more extreme if the paddle makes contact
#with the ball in an upper or lower portion than when compared to if the ball hits the middle
#of the paddle. If the ball hits the middle of the paddle, it will rebound at a normal pace with
#a slight y-step for the ball. For each respective zone, the ball's x and y steps are not the exact same.
#It can vary between three speeds, each of which are very close together. The only exception to this is if the 
#ball hits the middle zone of a paddle, it will keep its y step but its x-step will be either 13 or -13 depending
#on which paddle it hit. If you choose one player mode, you will be playing against
#AI. Based on the difficulty chosen, the AI will get better or worse. The AI has three factors 
#that determine its performance. The first is known as response. As soon as you make contact with the
#ball, the AI knows where the ball will end up. The response determines when the AI can start
#moving towards the balls destination. The AI predicts where the ball will be based on an algorithm that
#takes into account the ball's x-step when it makes contact with your paddle and uses that to determine
#how many times to add up the y-step. In order to account for if the ball hits walls on its way
#across the screen, the algorithm will start to add -1 * the y-step if the predicted y value goes
#below 0 or above the height of the canvas. When the algorithm is complete, the AI know the y-coordinate 
#where the ball will intersect with the x-position of the outermost part of the AI paddle (the right paddle).
#For all of the difficulties, the response is the same; the AI will start to move after the balls x-location is greater than 400 with 
#respect to the canvas. The second factor that the AI uses is known as recovery. What recovery does
#is it tells the AI paddle to recover toward the middle of the screen after it makes contact. Thus
#it will have a smaller average distance to travel towards the ball. Recovery is turned off in easy difficulty,
#but turned on in normal and insane difficulies. The third factor that the AI uses is the speed that it can move to the ball.
#In my code, I represent this term as AILEVEL. What it represents is the paddles y-step when it moves to the ball.
#In easy mode the AILEVEL is 18, In normal mode it is 20, and in insane mode it is 34. This is the most important factor
#for the AI, and is the main reason why it is so hard to win on insane mode. Seperate from AI, a
#fourth factor that contributes to the difficulty chosen is the speed that the ball moves. I represent 
#this in my code as SPEED. Since the changeBall function always returns the same random values depending on the zone
#of the paddle in which you hit, by multiplying SPEED by these values, you can succesfully modify the x and y steps of 
#the ball without messing with the proportions by which it travels. In easy mode the SPEED is set to 2.4, in normal mode
#the SPEED is set to 2.9, and in insane mode the SPEED is set to 3.2. If you get bored of playing against AI,
#you can choose to play against a friend by selecting 2 player mode. This mode allows each player to control 
#a respective paddle. If you want to change the speed of the ball in tow player mode, you
#can change the difficulty and the ball speed will be matched to the SPEED set in the selected difficulty settings.
#I also used a few global variables to keep factors such as the paddle speed for your paddle in one player mode
#constant as well as the paddle speed for both paddles in two player mode constant. In addition to
#the paddlespeed I also have global variable for the score the games are played to and teh response for the AI.
#Enjoy. 
