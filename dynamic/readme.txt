__init__.py:
    used to make this directory as a module 'package'
    and user can import this module.

wsgi_app_frame_dictionary.py:
    used to recv dynamic msg to assemble response body
    and return it to Server

Functionility:
1. register user:
    + create a new normal user in mysql
        - only have search right to total dictionary view (v_dict)
    + and also create a new table "user_tb":
        - all rights (add, delete, update, search)
2. login: connect user to mysql

Dictionaries:
1. total dictionary:
    + user cannot change anything, only root user(me) can
    + make a new "view" table for all users:
        - make it easy to search to normal users(search word from v_dict then add)
    + create "index" for the view "v_dict":
        - make it fast for searching
2. search dictionary:
    + normal users have all rights
        - search: !! (add a new button in nav to search in search tb)
            * further more add a google search button
        - delete/update:
            * directly done in pop-up window
            * and delete/update in search_tb in mysql
        - add: add to Taks page (cross the box)

Search/Add Process:
1. inside Home page:
    + total dict (cross box and submit) -> "New Add" tb(local storage)
    + search word (total dict/search dict)
    + Add new word (below nav) -> add to "New Add" tb(local storage)
2. so no matter the word is exist or not in search table,
    "search" or "add" the "freq" will always record "+1" time!
    but difference is:
        + search: only show search result (not add freq)
        + add: freq + 1, and add to "New Add" tb(local storage)
3. All words in "New Add" tb -> Search table in mysql database.
/*
Abandoned! NOT GOOD, keep ONE BUTTON for ONE FUNCTION
2. from Home page to Task page:
    + search new word (total dict/search dict) -> "New Add" tb(local storage)
*/