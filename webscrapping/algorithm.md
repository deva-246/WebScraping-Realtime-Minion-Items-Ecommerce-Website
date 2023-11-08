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
 
7. To get your own user agent visit **www.whatismybrowser.com** > User Agents > Parse your Agent. Now click the link and copy and   
       paste it in the python code.

8. Fit the above mentioned components in the below code,
  
        URL = 'Link of the desired category of your target website'
  
        HEADERS =  ({'User-Agent' : 'YOUR USER AGENT'})

        webpage = requests.get(URL, headers= HEADERS)
