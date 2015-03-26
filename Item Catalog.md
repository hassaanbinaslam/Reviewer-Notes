### A note from Adam Piskorski on Storing Images in the Database
 I recently 
learned that storing images in your DB is seldom used and not a good 
idea for sites that receive a lot of traffic, whereas it's much better 
to store your images in the file system and store references to their 
paths in the db. 
There are many reasons, among those are the fact file systems are 
optimized for handling large files, whereas DBs are better at handling 
many smaller requests and the fact that precious DB performance can 
quickly become lost unnecessarily because of a potentially huge number 
of images.

There are many more reasons, which you can read about in a superb 
StackOverflow page on it here: 
http://stackoverflow.com/questions/1234202/storing-images-db-or-file-system 
I've never deployed a webapp that needed to serve many images and I 
naturally thought storing them in the DB was the best way, but given all 
of the above, I'll also update my own webapps now to follow this better 
practice!

It's actually quite easy to store files on the file system with your 
webapp, especially if you use a library such as the nice flask 
extension, Flask-Uploads: https://pythonhosted.org/Flask-Uploads/


