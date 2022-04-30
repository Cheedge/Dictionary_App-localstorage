Vocabulary Remember App
version: 0.1
author: CheedgeLee
Descreption:
...



TODO:
Templates realize:
1. Basic: 2 page:
    (1) Task page: 2 tab tags
        + navbar: Search (add to searched list)
        + today list (random list 100 words with pass button)
        + remembered list (order by search order 100 with need remember button)
    (2) Home page: 2 tab tags
        + navbar: add form ("vocab and translate" then add to total dictionary)
        + searched list (order by search times with remembered button)
        + total dictionary (order by alpha-beta, with add button)
2. More:
    + search/total list separate into pages
    + login/logout
        - different user with different vocabulary table list(same database)
    + show the frequency graph
    + test and check
3. Advanced:
    + show some similar words

Process:
1. search mysql database (search order 100)-> local storage-> remembered list
2. total mysql database (random 100)-> local storage-> today list
3. search mysql database -> search list
4. total mysql database -> total list
Notice:
    mysql(total) -> html(table) -> js(get 100 from table) -> local storage(str)


Search Process:
    search -> total mysql database -> add to search mysql database
Add Vocab Process:
    New vocab -> total mysql database

Database:
    1. total database: (German, English, Notation)
    2. search database: (German, English, Notation, Freq.)

Advance:
    1. off-line NLP training find similar words (semantic or written)
    2. according to above NLP training:
        + provide the similar words of high freq. words for every dictionary
        + when search a word, give similar words
    3. web crawler find sentances.