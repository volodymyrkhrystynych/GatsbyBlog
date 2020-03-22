# Bootstrapping a data-driven application with Zappa to find an apartment in Toronto
# 2020-02-27 Thursday
## Myplanet building

https://ServerlessToronto.org
# Ian Whitestone

## Intro
 - Trend Micro is sponsoring the event and provided food
	 - Organization are struggling to incorporate and transition into the cloud
	 - The other difficulty is that organizations must be compliant
	 - The combination of these two difficulties are what Trend Micro specializes in solving for Companies
	 - They have tests to check in a companies cloud solution complies with the regulations

 - He built this in 3 days

## Main Talk
### Ian Whitestone

#### Intro
 - Main catalyst for the talk is that he was able to launch a data heavy web application very quickly
 - Inspired by a San Francisco application where a guy made a bot that posted links on slack for the houses that make sense
 - Also inspired by the housing prices in Toronto
   
 - You can add apps to Slack
 - There is a selection for choosing what area you want to get listings from

#### Center
 - Serverless : Not no servers but No permanent servers you have to manage
	 - Instead you just write code and invoke that code on demand
	 - Azure function
	 - Google could functions
	 - IBM cloud functions
	 - AWS Lambda
 - Requirements for Ian:
	 - No knowledge or maintenance of servers
	 - Run periodic batch jobs
	 - Respond to api requests
	 - Cheep and easy
 
 - You need to setup a handler function that is what is called every time your service is called using lambda
 - Setup AWS AIM ( user management )
 - Cloudwatch is like a cronjob for the could, do things on a schedule

 - he needed to change file permissions in order for it to not break

 - psycopg2 package is used to save to a database
 - Lambda functions on a pre-configed Amazon Linux Machine
 - Certain libraries need to be pre-compiled on Amazon Linux
	 - Docker or Popular libraries 

##### Zappa
https://github.com/Miserlou/Zappa 

 - Flask or Django use Zappa
 - Zappa has a settings json that needs to be configured.
 - Basically automatically does all the previous stuff, setting up AIM, lambda function etc.
 - zappa tail dev : to get logs in the terminal
 - zappa dev " python code " --raw : runs the python code you write in a string in order to help debug
 - By default zappa keeps your server warm (always ready)
 - AWS currently limits Labmda zip sizes to 50 megabytes
 - Zappa uploads the packages to S3 in order to overcome the limitation that some packages like pandas cause (being 50 megabytes already)
 - There are other serverless frameworks, he used zappa since he didn't want to learn to debug javascript
	 - Serverless
	 - Chalice
###### Downsides
 - Very few active maintainers (though an active slack community)
 - Not really doing much feature development
 - Vendor lock-in with AWS
 - No support for AWS layers
 - Pre-compiled dependencies support isn't great


##### Data science part
 - Data Difficulties:
	 - variance for 1 bedroom is smaller than variance for 3 bedroom
	 - Number of bedrooms has a disproportionate impact on price
	 - Location data is difficult to model as lat long do not have a linear relationship with price
		 - He used the neighbourhood as a substitution for location, he used clustering to group the neighbourhood 
		 - Used nearest neighbours instead:
			 - Retrieve X nearest apartments with same # of bedrooms
			 - Calculate mean, median etc
			 - Feed that into model
			 - Used Annoy (Approximate Nearest Neighbors Oh Yeah)
			 - Can also use SKLearn
 - Settled on Quantile regression as it let you ask for median, 

##### Additional things that could have been done 
 - Add a weighting to the nearest neighbors and how the data contributes, to handle the scenario where you have an outskirt listing
 - Adding user readable output, instead of (1200 is a normal price) (the normal price for an apartment with this number of bedrooms in this area is between 1000 and 2000)
 - Add expectations for the data in order to track that the data sources and your code is working properly, ie there should be at least x listings a day, or there should be an expected number of null values

##### Gotchas
 - when you do a cold start for the first time it runs an init function:
	 - if a transaction fails once then the subsequent 
	 - Fix: make a fallback function that catches the exception and tries to rerun the init
 - Slim handler kills performance on cold starts:
	 - When useage spikes the new machines that aws runs are all going to cold start first
	 - Used a regex function to remove some of the heavy packages in certain situations




