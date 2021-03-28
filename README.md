# AutoTrader Car Data Scraper
# Qihan Guan, Michael Harris, Luyao Wang
----------------------------------------


# Overview
-----------------------------------------
Our project entails building an automatic web scraper that can scrape data for listed vehicles on Autotrader.com 
based on the user’s inputted search criteria. Our program first asks the user to input the year, make, and model 
for the car they would like to search. The user is then asked to input the search area's zip code and the radius 
in miles. After taking the user's input, the program constructs a specific URL and processes a GET request to obtain 
the URLs for each vehicle listing that matches the user’s search criteria. The program then downloads these URLs as 
‘.html’ files and scrapes data on vehicle specs, price, and seller information. This data is first saved in a data frame 
before being loaded into a MongoDB database. Finally, the program queries the MongoDB database and outputs summary 
statistics to aid the buyer or seller in making an informed decision. 

# Run the code
-----------------------------------------
*To start a brand new scraping task, simply open the ipynb file and click run all cells.
 Please make sure to install all the required packages. 

*The program will then ask you to input specific information:
 1.Enter Make(Press enter directly to omit):
   --For this step, please enter a car brand, Toyota, Honda, BMW, etc.
     Please make sure the brand is a valid brand. 
     If you want to scrape a full dataset with no brand specified,
     then press enter directly to leave this blank.

 2.Enter Model(Press enter directly to omit):
   --For this step, please enter the desired model for the car brand
     that you just chose. If you input Toyota in step1, you can
     enter Camry for this step. Please make sure the model is a 
     valid model under the brand you chose in step1.
     If you search all models under the brand in step1, then press enter
     directly to leave this blank.

 3.Please enter vehicle minimum year: (1981-2021):
   --For this step, please enter a valid year between 1981 and 2021.
 
 4.Please enter vehicle maximum year: (1981-2021):
   --For this step, please enter a valid year between 1981 and 2021
     and the year must be greater than or equal to the minimum 
     year you just inputed.

 5.Please enter your 5-digit Zip Code: 
   --For this step, please enter a desired search area zip code.
     The program will automatically validate the zip code.

 6.Please enter your search radius in miles (10/25/50/75/100/200/300/400/500/ 0 for any):
   --For this step, please enter a number in the list. The program will keep
     asking you for the valid input if you do not enter it correctly.

*After the input are taken. The program will take over for the rest.
 It will automatically scrape the data and save them to a MongoDB database.
 In the end, it will return some summary stats as well. 
