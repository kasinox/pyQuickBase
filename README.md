pyQuickBase
=========

pyQuickBase is a Python interface to the QuickBase API. The modules adhere to the QuickBase API call naming convention, written in the Python syntax. Requests are made with [**Requests.py**][requests], and [**lxml**][lxml] is used for XML processing.

This project is a work-in-progress. I started this project hoping to build a performant, reliable Python client to QuickBase to use for my day job. It supports tokenization, SSL, realms, and most other commonly used options. I appreciate feedback and would love to have another developer help improve the project.

This project is a fork of Oyster.com's QuickBase interface, available on [**github**][oyster], with significant changes (and being actively developed). The original license is included in the license file.


Version
-
0.2

API Features
-----------
+ do_query
+ do_query_count
+ granted_dbs
+ add_replace_db_page
+ edit_record
+ add_record
+ get_db_page
+ list_db_pages
+ import_from_csv
+ delete_record
+ get_schema


Helper Functions
-----------
+ get_file -- used in conjunction with a query and specified attachment field ID, can download one or many files from a table to local folder.

Requirements
-----------
* Python (2.6+)
* [lxml]
* [Requests]
* chardet
* cStringIO

Examples
--------------
    client = quickbase.Client(username, password, database=dbase, apptoken=token, base_url=url)
    response = client.do_query(query="'3'.XEX.''}", structured=True, columns='a', database='yourdbname')
    for r in reponse:
        print r

License
-
MIT, See license file.

Developed by [**Kevin V Seelbach**][ks]. Contact me by email at [kevinseelbach@gmail.com][ks].

  [requests]: http://docs.python-requests.org/en/latest/
  [lxml]: http://lxml.de/
  [ks]:kevinseelbach@gmail.com
  [oyster]: https://github.com/oysterhotels/quickbase
