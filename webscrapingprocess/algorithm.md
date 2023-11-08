## Steps to perform webscrapping using python

1. Open jupyter notebook and create a project folder
 
2. Open a python file to perform web scrapping
   
3. Import the below mentioned packages

       BeautifulSoup

           pip install bs4
            
       requests

            pip install requests
   
       pandas

           pip install pandas
   

4. Go to the required website and search for the category that you want to scrap
   
  
5. Now right click > inspect and examine the html code present in the window that is displayed in the left end of your screen
   
  
6. For any webscrapping using python 2 main components are important to make a http request using HEADER,
  
        > UserAgent 
        
        > Page URL
 
7. To get your own user agent visit **www.whatismybrowser.com** > Detect my settings > User Agents > Parse your Agent. Now click the link and copy and paste it in the python code.
   

8. Fit the above mentioned components in the below code,
  
        URL = 'Link of the desired category of your target website'
  
        HEADERS =  ({'User-Agent' : 'YOUR USER AGENT'})

        webpage = requests.get(URL, headers= HEADERS)
   

9. Check the Success of HTTP Request by printing the webpage variable

       > if output is <Responese [200]> - SUCCESSFULL

       > else if output is <Responese [503]> - Try again later with a different user agent / alternate website link
   
10. Now, the website HTML content is recieved from the website in bytes type, so we must convert it into proper HTML format this is achieved by using BeautifulSoap(),

       any_soup_variable =  BeautifulSoap(webpage.content , "html.parser")

11. Determine the code of required component details that you are in need of, for example:

        > Product Title

        > Product Price

        > Product Rating

12. Find out the tag and class name for respective component by using inspect option to extract the data, and store them.

       any_soup_variable.find("tag name", attrs={"class/id" : 'respective name'})

    by this command respective tag details will be displayed, to alter the output .text.strip() can be used to the above line of code.
       
13. To get these data into a csv file , extract data and store it in a list and define function to get the tag data respctively.

14. use this command to transfer all the data into a csv file,

       dataframe_name.to_csv("minions.csv", header=True, index=False)

      

