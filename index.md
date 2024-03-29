# Caleb Wilson

### Welcome to my personal github portfolio!

Hello my name is Caleb Wilson and I am an applied mathematician. I like math, programming, machine learning, and strategy games. This github portfolio is here to showcase some of my work. You can check out the rest of my profile [here](https://github.com/lodeous).

### Risk Game analysis with PyRisk

<img src="cm_aggregate.png" alt="Confusion Matrices for classifiers" class="inline"/>

<small>**Above:** A comparison of different classification methods used to predict the winner of a risk game. The Confusion
matrix shows how many times they classified a certain player winning vs which player actual won. The dark blue diagonal
indicates that the classifiers performed well.</small>

For a school project, my group and I set out to analyze Risk gameplay and predict a winner based on an unfinished game.
We found an open source engine written in Python called PyRisk that had the capability for different computer bots to play 
Risk against each other. We forked the repository and made changes to generate lots of game data. Then we wrote code to parse
that data into Pandas dataframes. We engineered features like continent control, some graph based features, and troop count
features. Then we applied several machine learning classifiers, like Random Forests, Logistic  Regression, K-nearest
neighbors, and XGBoost to try to predict the winning player. We ran grid searches to find the optimal hyperparameters for
training the classifiers. We used the Random Forest classifiers we trained to show us which features were more important in
predicting the data. We also visualized the data we collected with a t-SNE projection.

I modified PyRisk to run games in parallel so our data generation would be faster. I also wrote code to run logisitic
regression, random forest, and k-nearest neighbors classifiers on the data to predict the winner. Because the data we
collected was high-dimensional, I used Principle Component Analysis to reduce the dimensionality of the data before feeding it
to the k-nearest neighbors classifier. For a fuller explanation, please see the report linked below.

 - [Repository](https://github.com/LukasErekson/pyrisk)
 - [Report (PDF)](RISK_Data_Project_Fall_2020.pdf)

### Gravitational Slingshot physics simulation

<img src="slingshot_options.png" alt="A plot several different slingshot trajectories" style="padding: 1% 4%;"/>

<small>**Above:** By varying the initial velocity slightly, we were able to plot out several different possible slingshot
trajectories for a satellite in our model. While this is plotted in 2d for simplicity, we also did some 3d simulations,
plots, and animations.</small>

For a school project, my group wrote python code to simulate gravitational attraction in an n-body system.
Then we found initial conditions that would allow a small or zero mass object to slingshot off of a more massive object,
like in space missions. We ended up with some cool results and with code that given an initial guess could find an initial
velocity to slingshot an object to a trajectory that would approximately pass through some desired point in space.

I wrote 2d and 3d plotting and animation code, including initial/final velocities, energies, and an acceleration vector
field. I also helped find initial conditions that led to a gravitational slingshot.

 - [Repository](https://github.com/samcochran/optimal-spacecraft-control)
 - [Animations](https://samcochran.github.io/optimal-spacecraft-control/nbody_slingshot.html)
 
### Optimal Spacecraft Control in an n-body system

<img src="second_control_attempt.png" alt="Optimal control example" class="inline"/>

<small>**Above**: Here you can see one of our optimal control solutions. The thrust control descibed by u1 and u2 on the second graph shows the
optimal thrust of the spacecraft over time. Here you can see it is optimal for it to spend all of its thrust at the beginning as it passes by the sun.
Looking at the animated version (see link below), you can see that it thrusts towards the sun to maximize its velocity gain as it slingshots past the sun.</small>

Building off our previous slingshot project, my group solved an optimal control problem that minimizes the amount of fuel and time it takes for a spacecraft
to get close to a target destination. I helped in the mathematical formulation of the problem, adding mass as part of the state equation, finding a difficult vector derivative,
rewriting the control from polar coordinates to euclidean coordinates, and contributing ideas that allowed us to solve for our optimal control linearly in terms of the costate.
For those unfamiliar with the math jargon surrouding optimal control, it was important that we found a linear solution to the optimal control because allowed us actually find a
solution to our optimal control (and in general it makes your problem more tractable). Previous attempts with a nonlinear solution took a long time to calculate with the added 
bonus of not converging to a solution after the hours-long calculation.
Once we got to the coding part of our project, I wrote most of the solution code that implements the optimal control problem as a boundary value problem solved with scipy's `solve_bvp` function. 
In addition, I wrote the base code for plotting and animating the solutions, which was then expanded upon by my teammates.

 - [Repository](https://github.com/samcochran/optimal-spacecraft-control) (same as above)
 - [Animations](https://samcochran.github.io/optimal-spacecraft-control/)
 - [Report (PDF)](Math_438_Project.pdf)
 
### General Conference Topic classification and talk recommendation

As a group project in college, my group and I set out to classify general conference talk topics and recommendation talks based on their topics. These talks
were taken from the Church of Jesus Christ of Latter Day Saints, which holds a "general conference" twice a year. We scraped talks from the Church's
website www.churchofjesuschrist.org as well as from the website scriptures.byu.edu which had easy to parse versions of the talks for a longer period of time.
I wrote the code to scrape the talks from scriptures.byu.edu. I also wrote code that utilized nonnegative matrix factorization to create a recommender system.
I assisted in training Random Forest classifiers to classify topics based on the output of an unsupervised Latent Dirichlet Allocation Collapsed Gibbs Sampling
performed on the talks.

For a full explanation of the project and the results, please see the report below.

 - [Repository](https://github.com/lodeous/gencon-nlp)
 - [Report PDF](FINAL_General_Conference_NLP_21.pdf) 
 
### UniWar

UniWar is an online multiplayer turn based strategy game. I worked part time to fix bugs and add new features to the app.

 - [UniWar Website](https://www.uniwar.com)
