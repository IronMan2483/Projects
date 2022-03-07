# __King County Real Estate__

This notebook is about my first EDA project. You find the [notebook](https://github.com/IronMan2483/Projects/tree/main/Project_1/notebooks) in the notebooks folder. Created images, plots and maps are in the [images folder](https://github.com/IronMan2483/Projects/tree/main/Project_1/images).

The task: You'll be working with the King County House Sales dataset. Here, the focus is on EDA though you are required to demonstrate an entire Data Science Lifecycle using linear regression.
Your task will be to perform an extensive EDA and to train a explanatory linear regression model. The task is not only to explain the data but also to evaluate how well the model is fitting the data. For a more detailed task description have a look at the assignment.



#### __Where is King County?__ 
King County is located in the U.S. state of Washington. The population was 2,269,675 in the 2020 census, making it the most populous county in Washington, and the 12th-most populous in the United States. The county seat is Seattle, also the state's most populous city.
King County is one of three Washington counties that are included in the Seattle–Tacoma–Bellevue metropolitan statistical area. (The others are Snohomish County to the north, and Pierce County to the south.) About two-thirds of King County's population lives in Seattle's suburbs. (definition source: wikipedia)


![Seattle Skyline](https://github.com/IronMan2483/Projects/blob/main/Project_1/images/wallpaperflare.com_wallpaper.jpg)
###### source: wallpaperflare.com


---

## __The Deliverables__
* New repository from template
* A well documented Jupyter Notebook (see here for an example) containing the code you've written for this project and comments explaining it. This work will need to be pushed to your GitHub repository in order to submit your project. Do not push all the analysis... just the analysis that is relevant!
* An organized README.md file in the GitHub repository that describes the contents of the repository. This file should be the source of information for navigating through the repository.
* A short Keynote/PowerPoint/Google Slides/Jupyter slides presentation giving a high-level overview of your methodology and recommendations for non-technical stakeholders. The duration of the presentation should be 10 minutes, then the discussion will continue for 5 minutes. Also put your slides (delivered as a PDF export) on Github to get a well-rounded project.
* Optional - A Python script for training the model, printing out the model statistics and saving the model. Look at this stackoverflow discussion on how to save a statsmodel.

---

## __Stakeholder__
We get to know our stakeholders. I selected the following one:
* name: Jacob Phillips
* stakeholder: Buyer
* characteristics: Unlimited Budget, 4+ bathrooms or smaller house nearby, big lot (tennis court & pool), golf, historic, no waterfront

So it is most important for this stakeholder especially - so not only for every property in Real Estate:
__"Location, location, location!"__
It is the RE agent's mantra which means that homes can vary widely in value due to their locations. Location is essential when it comes to the value of a property.

---

## __My Hypotheses__

* My stakeholder wants a house without waterfront. This will be difficult because Seattle is surrounded by water.
* Am I able to present more than 1 house that meets all of his criteria?
* If so, should I focus on the golf clubs as well? But most of them are in Southern suburbs of Seattle.
* Are the historic houses also in the fancy, expensive and safe districts?
* Does historic houses have more than 4 bathrooms?

---

## __What should be defined?__
I need to define the following ones in my notebook to be able to provide suitable recommendations to my stakeholder:
* what means unlimited budget? - price query over min. US$ 1 mio.
* what means big lot? - sqft_lot, besides that also sqft_living sqft_above and sqft_basement. As a Non-US citizen I am not used to understand/work with square feet. So I need to add a new column and convert the values to square meters. 
* where can I see if a tennis court or pool is included? - sqft_lot and google maps satellite
google for best districts/zip codes - zipcode
* where are the golf clubs / green fields nearby? - zipcode
* what means historic houses? and when was the last renovation? - yr_built and yr_renovated. I will use queries and filter for houses built before 1980 and a second one for houses built before 1960.
* number of bathrooms: 4 or more - sort and query.

---

## __Benchmark/comparision__
I just wanted to have an understanding of relevant prices, lot and house sizes. So I did some research to have a benchmark.
* Meghan and Harrys home in Montesito has a lot of 7,4 acres (3 hectar = 30,000 m2) and a living lot of 18,671 sqft (1,735 m2) for US$ 14.65 million: The 18,671-square-foot home boasts 16 bathrooms and nine bedrooms, not to mention a tea house, two-bedroom guest house, pool, tennis court—and a chicken coop, as seen during their tell-all interview with Oprah. This Mediterranean-style dwelling, which was built in 2003, also features its own movie theater, elevator, arcade room, wet and dry sauna rooms, a gym, library, and other impressive amenities.
* Cristiano Ronaldo bought an apartment in a great district in Madrid for US$ 8 million and a living lot of 1000 m2 (10,763 sqft)
* One of Bezos’ first homes he purchased was/is in Medina, Seattle. He paid $10 million in 1998 for a 20,600-square-foot, five-bedroom, four-bathroom house, according to Realtor.com. The 5.3-acre property in the ritzy Seattle suburb is located near the local Post Office and grocery store, property records show. Then, in 2005, he reportedly spent $50 million on a neighboring 8,300-square-foot mansion with five bedrooms and four bathrooms. The properties have a combined 310 feet of shoreline, according to Realtor.com. Finally, Bezos plunked down $28 million in renovations on the combined estate in 2010, according to Realtor.com, for a total of $88 million spent on the estate — $118 million, adjusting for inflation. Medina Peninsula is accessible from Seattle via the longest floating bridge in the world, spanning 7,710 feet across Lake Washington. The 1.4-square-mile city has a golf and country club founded in 1927, where residents like to not only golf but swim and play tennis, according to Mansion Global.
* Bill and Melinda Gates have a $127 mansion in Medina, WA, which is about 15 minutes from Seattle. (data from 2019)

---
 
## __Workflow steps__

1. Import mandatory tools and libraries
2. Read the file and get an overview of the data
3. How does our properties portfolio looks like?
4. Get an understanding of the column names or the 'real estate language'
5. Get an understanding of the relevant/suitable districts in the Seattle area (Seattle and its suburbs)
6. Create an overview of our houses
7. Get an understanding of the data with plots
8. Locations of all of our properties
9. Filter with a query for our price ranges: 0-25%, 25-50%, 50-75% and 75-100%. For houses with a price of min. US$ 1 mio. in 1 mio. steps.
10. Filter with a query with 3 of the stakeholders's must-haves for his future home: 4+ bathrooms, size and no waterfront
11. Get an overview of our available properties in the 10 suitable districts - query by district
12. Get an overview of all properties in the relevant 10 districts with 1 query
13. Filter for historic houses in the relevant district list: houses built before 1980 and houses built before and in 1960. 
14. Create a presentation for the stakeholder with 3 recommendations → see [Jacob Philipps Portfolio](https://github.com/IronMan2483/Projects/blob/main/Project_1/Stakeholder_JP.pdf)

---

# __Technical preparation__

### __ds-project-template__
Template for creating ds simple projects 


### __Requirements__

* pyenv
* python==3.9.4

### __Setup__

For this purpose you use following commands:

```bash
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### __Remarks__
Data or Models folder content should not be pushed to github.
