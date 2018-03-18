# Udacity FSND Project - Catalog Application
The project creates a catalog database, populates it with some sample data and demonstrates CRUD operations and 3rdparty authentication. The project is based on the Flask framework. The project contains the following content
* **database_setup_catalog.py**  - Python script to create the catalog.db.
* **sampledata.py** - Python script to add sample data to the database
* **project.py** - Main application python script
* **client_secrets.json** - File containing Google authentication informations
* **fb_client_secrets.json** - File containing Facebook authentication informations
* **README.md** -  This file specifies details about the project and how to run and access the application.
* **catalog.json** - This file contains the sample JSON endpoint output.
* **catalog.db** - Sample Database to launch the application directly
* **templates** - Contains the different html templates for rendering of the different Flask routes
* **static** - Contains the css files

# Requirements
* Python 2.7 (Not tested with other versions of Python)
* Postgresql
* Virtualbox
* Vagrant

# Install
* Install [Vagrant](https://www.virtualbox.org/wiki/Download_Old_Builds_5_1) and [Virtual Box](https://www.vagrantup.com/downloads.html),  if you have not done so already. Instructions on how to do so can be found on the websites as well as in the course materials
* Clone the fullstack-nanodegree-vm repository.
* Launch the Vagrant VM (by typing vagrant up in the directory fullstack/vagrant from the terminal). You can find further instructions on how to do so here.
* Clone the repository using the command
* `git clone https://github.com/datechie/catalog.git`
* Install Python 2.7 from [here](https://www.python.org/downloads/release/python-2714/), if needed


# How to run
1. Go to the directory with the code
- `cd catalog`

2. **OPTIONAL** - If you do not want to use the existing catalog.db and would like to create a fresh one.
- `rm cataglog.db`
- Create the database (catalog.db)
- `python database_setup_catalog.py` **OR** `python2.7 python database_setup_catalog.py`
- Populate the database with some sampel data
- `python lotsofcats.py` **OR** `python2.7 python lotsofcats.py`

3. Run the application
- `python project.py` **OR** `python2.7 project.py`

4. To review the page, launch  http://localhost:5000 in your Chrome browser

# Details (as per the project rubric)
1. **JSON Endpoint** - http://localhost:5000/catalog.json will show the JSON details of all the current category and item data in the database

2. **CRUD Read** - Launching http://localhost:5000/ or http://localhost:5000/catalog reads and shows the data from the catalog database

3. **Authentication and Authorization** - The project implements Google and Facebook authentication. Only authenticated users, can see the create, edit, delete options for the records. Further, they can only edit/delete records created by them and not by others (this displays a Flash message and takes them to the home page). The initial sample data will not be editable by anyone.

4. **CRUD Create** - When a user is authenticated, they can see the Add item link on the http://localhost:5000/ home page below the listing of the Latest Items. The Add Item option takes them to Add a new catalog item page, where users can add name and description and select the cataegory from the existing drodpown list (there is no option for a user to Add a new category.)

5. **CRUD Update** - For an authenticated user, when they drill down to the catalog item, there are two options Edit|Delete. The Edit option takes you to the Edit Item for - name, description and category can be updated. The category is a dropdown and you can change categories. The Save option will update the record and show an appropriate Flash message. Cancel will discard all changes and take you back to the home page.

6. **CRUD Delete** - As 5 above, for an authenticated user, when they drill down to the catalog item, there are two options Edit|Delete. The Delete option takes you to the Delete Item for form for confirmation. The Delete option will delete the record and show an appropriate Flash message. Cancel will keep the record and take you back to the home page.

7. **Pep8 compliance** - The 3 python scripts have been tested with pep8 and are compliant. Have also tested with pycodestyle and it shows one message - project.py:244:5: E722 do not use bare except' - this does not happen with pep8 and so has been ignored.

