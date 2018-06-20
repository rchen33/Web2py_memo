Running the file:

1) Download the Web2py_memo repository. 
2) While in current folder, type python web2py.py -e on the command line.
3) Once a pop up appears, type in your password of choice.
4) Click start server. 
5) The website should load on browser. 

Important files:

1) tables.py: Found in applications/start/models/tables.py
	- Keeps track of the logged in users
	- Initialize memo database
	- Defines the fields for each memo

2) api.py: Found in applications/start/controllers/api.py
	- Controlls the memory in the database
	- Has functions that work directly with the database defined in tables.py
	- add_memo(): Adds a new memo to the database
	- get_memos(): Retrieves all the memos from the database
	- del_memo(): Deletes a memo from the database
	- toggle_public(): Changes the field is_public boolean in the database

3) default_index.js: Found in applications/start/static/js/default_index.js
	- Holds all the important data and methods in self.vue
	- Functions like self.add_memo not only adds a new memo to the list self.vue.memos, but also to the database. It adds to the database by passing variables into the function add_memo() in api.py.
	- Functions like self.get_memos() calls the function get_memos() in api.py to get a list of all the users from the database.

4) index.html: Found in applications/start/views/default/index.html
	- HTML file that designs the outline of the website.
	- calls all the vue functions and variables. 