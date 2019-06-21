Item Catalog

About :
This project is a RESTful web application utilizing the Flask framework which accesses a SQL database that populates 
categories and their items. OAuth2 provides authentication for further CRUD functionality on the application. Currently OAuth2 is implemented for Google Accounts.

In This Repo :
This project has one main Python module app.py which runs the Flask application.
A SQL database is created using the database_setup.py module and you can populate the database with test data using database_init.py. 
The Flask application uses stored HTML templates in the tempaltes folder to build the front-end of the application. 
CSS/JS/Images are stored in the static directory.

How to Install :
1-Install Vagrant & VirtualBox
2-Clone the Udacity Vagrantfile
3-Go to Vagrant directory and either clone this repo or download and place zip here
4-Launch the Vagrant VM (vagrant up)
5-Log into Vagrant VM (vagrant ssh)
6-Navigate to cd/vagrant as instructed in terminal
7-The app imports requests which is not on this vm. Run sudo pip install requests
8-Setup application database python /item-catalog/database_setup.py
9-Insert  data python /item-catalog/lotsofmenus.py
Run application using python /item-catalog/project.py
Access the application locally using http://localhost:8000

Using Google Login :
To get the Google login working there are a few additional steps:
1-Go to Google Dev Console
2-Sign up or Login if prompted
3-Go to Credentials
4-Select Create Crendentials > OAuth Client ID
5-Select Web application
6-Enter name 'Item-Catalog'
7-Authorized JavaScript origins = 'http://localhost:8000'

JSON Endpoints :
The following are open to the public:

Catalog JSON: /catalog/JSON - Displays the whole catalog. Categories and all items.

Categories JSON: /catalog/categories/JSON - Displays all categories

Category Items JSON: /catalog/<path:category_name>/items/JSON - Displays items for a specific category

Category Item JSON: /catalog/<path:category_name>/<path:item_name>/JSON - Displays a specific category item.