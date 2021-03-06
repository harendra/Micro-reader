Very simple web based RSS/Atom reader, written in Python and [Bottle](http://bottlepy.org/). 

Try it out by installing requirements `pip install requirements.txt` and 
run `python microreader.py` . Then access http://localhost:3000

Runs on [Apache with mod_wsgi](http://bottlepy.org/docs/dev/deployment.html#apache-mod-wsgi).
An example app.wsgi is included in the repository.

To have automatic aggregation of feeds every five minutes, enter the 
following into crontab:
`*/5 * * * * wget -O - -q -t 1  http://<host>:<port>/channels/update`. 
Replace `<host>` and `<port>` with corresponding values.

A JSON api is available for most url:s, by adding `application/json`
to the Accept header.

![Microreader](http://morganbengtsson.github.io/images/microreader.png "Microreader")
