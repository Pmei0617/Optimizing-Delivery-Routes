# Optimizing-Delivery-Routes

Hi, my name is Peter Mei. The work shown here is an optimization model which I worked on with Binhao, Chen. The learning objective of the project is to showcase how Mixed integer linear program can be applied to solve a logistics problem. In doing this, we have chosen the min cost flow model to help optimize routes for a truck delivery case. In our business scenario, we want to find the cheapest delivery route from Texas to Washington for 6 different truck classes. This makes minimizing total cost our model objective. 

We started by extracting distance between each contiguous states using Google API in Python. We then assigned a binary decision variable to each state-to-state distance. 

In calculating total cost, we took fixed toll rates by truck class, toll rate per truck carrying capacity and fuel cost into consideration. The binary decision variables will help determine whether a path is chosen, and if it is chosen, we will consider its corresponding costs in solving the model. 

We set up a net flow constraint for each state as well as a check-up facility constraint to depict a business scenario where there should be equipment check-up for trucks that are in long distance operation. 

Lastly, we used Excel Solver to solve for the cheapest route for each truck class subject to constraints. The model was also deployed in python using the GLPK package in Pyomo. In visualizing the result, we used Plotly library to generate a map that shows the optimal route based on the truck class selected.  

### Steps to access the project
1. Open the Excel file to see how the model is set up using Solver
2. Open the Google Colab note book and upload the Excel file to see how the model is set up using Pyomo
3. There is a png showing the map output for truck class 5
4. Feel free to check out the poster which I submitted in one of our MSBA poster competition
