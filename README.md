# Web-Scraper-Project-Amazon

This project is a web scraping script written in Python. It is designed to scrape data from an Amazon product page, specifically the title and price of a t-shirt. The script uses the BeautifulSoup library to parse the HTML content of the webpage and extract the desired information.

The script begins by importing the necessary libraries, including BeautifulSoup for web scraping and smtplib for sending email notifications. It then sets the URL of the Amazon product page and defines the headers for making the HTTP request.

Next, the script sends a GET request to the URL and retrieves the page content. The BeautifulSoup library is used to parse the HTML content and find the elements with the desired information, such as the title and price.

The extracted title and price are cleaned up by removing leading and trailing spaces. The script also includes a timestamp to track when the data was collected using the datetime module.

The script creates a CSV file and writes the headers (Title, Price, Date) and the extracted data into the file using the csv module. It then uses the pandas library to read the CSV file and print the contents.

To continuously scrape the data at regular intervals, the script defines a function called "check_price()" that encapsulates the web scraping logic. The function is then called inside a while loop that runs indefinitely. The time.sleep() function is used to introduce a delay of 24 hours (86400 seconds) between each data scraping.

Additionally, the script includes a function called "send_mail()" that demonstrates how to send an email notification when the price of the t-shirt drops below a certain level. It uses the smtplib library to connect to a Gmail SMTP server and send an email with a predefined subject and body.

Overall, this project showcases how to scrape data from a website, store it in a CSV file, and automate the data collection process at regular intervals. It also includes an optional feature for sending email notifications based on certain conditions.
