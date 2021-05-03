## Creating an optimized route through Pittsburgh Breweries

I'm hoping to eventually clean this up more, but for now the code just lives in jupyter notebooks

### License requirements:
+ Sign up for a freemium account to use the [Here API](https://developer.here.com/pricing) 
+ obtain a license for [Gurobi](https://www.gurobi.com/academia/academic-program-and-licenses/)

### Initial setup
+ create a table of brewery information, like the one found in pitt_breweries.csv
+ create a file called "config.py", and define your api key like: api_key = 123456abcd
+ [configure your gurobi license](https://www.gurobi.com/documentation/9.1/quickstart_mac/retrieving_and_setting_up_.html) so the python package will run

From there, open a notebook, update the reference to read in the brewery list csv you created, and you should be able to execute the code chunk by chunk

Planned extensions:
+ currently the code just abandons the API call response for each route obtained during the step of gathering pairwise routes between all locations. It would be better to save these api response, so that once an optimal itinerary is found, the relevant API responses could be parsed out to deliver more useful information to the user (distances on foot, turn-by-turn directions, etc). 
