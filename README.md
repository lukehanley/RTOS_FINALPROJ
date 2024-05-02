# RTOS_FINALPROJ
Marble labyrinth game


WEEK 1:
So far the project seems like a lot to wrap my head around but breaking it down and doing this up front planning seems like it while be worthwhile, albeit tedious. At a certain point it is better to just start the project because we only know so much know, and as I start the meat of the project I will learn more that will change my plan. I built out a task diagram, risk register with two risks,  a couple unit test ideas, and a list of work items with estimated lengths. 

I like how I have the tasks set up, I think it breaks up a lot of the meat of execution into different tasks instead of having one massive physics engine task. 

Luke

WEEK 2:

Updated probability of senioritis risk because it is really starting to hit, as well as added a new risk that became apparent to me as I worked. Set up project overhead and intialized all data structures and tasks. Finished gyroscope task that updates the global var with both angles of the board rotation. Edited unit tests to make more explicit and testable. Added functional tests.

WEEK 3: 

Got the ball rolling around the screen based on the angle of the board, which knocks off a big functional test, and also means we are passing one of the unit test. Most of this weeks time spent on physics engine task and LCD task, as well as some time cleaning up the gyro task. As far as risk I added a risk for not getting system view to work on mac with probablility 100, so it is accepted. The work around is to run it on my windows desktop at home. I also mitigated the risk of too many mutexes for global info by using a sempahore to so the physics task can let the LCD task know that the ball's position has been updated. 

Just need to get the obstacles and collisions working, then I need to get the quantum working and we are most of the way done- I would describe this bare functionality as the minimum viable product. 

Changed plan to have collision checks occur in physics task as opposed to LCD task which will just update ball position periodically- thus LCD task is nearly done, just needs to have win conditions added and we are done. 

WEEK 4:

Put a lot of time into the maze this week. Created a struct type cell that has position and 4 walls, will likely also have integers for hole and waypoint. We have 48 cells that are pseudorandom and there is a maze on the screen. Close to getting collisions, will need to implement that in the physics task but it is largely based on how the maze is designed. The cells are structured in an array, but I was thinking about storing them in a BST or 2D array so that we don't have O(n) latency to check which cell the ball is currently in. 

Also cleaned up gyro task and physics bit to account for drift. 

Week 5:

Risk updates- changed collision latency risk "Own" description reflecting the plan to increase clock speed if it is an issue. Also changed randomzied obstacles risk to owned, as I am looking into and spent some time this week looking RNG using thermal noise from GPIO ports. I added a risk about me realizing that if I bomb the final project demo it won't actually affect my grade that much. I graduate in two weeks, so this project is starting to seem really insignificant.

Overall I only put in shy of two hours this week as we have our final capstone expo tomorrow Friday, April 27th, and that has eaten up pretty much all of my time this week. It's unfortunate, but unfortunately that has taken precedent over this project, as we have been scrambling all week to get things finalized. However, I should have some time this weekend and early next week to grind the project.

Week 6:

Didn't update anything. Senioritis risk did in fact hit. FInal product not working. Cheers.
