# Tracker — Basic Cloud Application Series
Track your geographical location.

How to use:
```
$ sudo docker run -d --env MAPKEY="your-map-box-key-here" -p 8000:3000 technomada/basic-tracker
```
Get a free map box key: https://docs.mapbox.com/help/glossary/access-token/  Use this token in "your-map-box-key-here".

### Explainer
This premise of this application is that there are times you'd like to track your location or your friend's or family but you wish to do so without sharing that location info with a public service.  With tracker your location is transmitted (using a mobile app) to your private server and the most recent points are plotted on an open (not commercial) map.


Transmission Client: (android)

https://play.google.com/store/apps/details?id=org.gnarf.bigbrother.gps
	
(or any app that can https post a json location object)

**Configure Client Url**
```
https://yourdomain.com/api/update/user-id-here
```

Replace ``user-id-here`` with your arbitrary user id (used later when viewing page.)

After a few data points have been posted from the transmission client

Open a web browser to...

https://yourdomain.com/#user-id-here  (``user-id-here`` is the same id as posted to /api/update/``user-id-here``)


![map with dots screenshot](https://github.com/technomada/basic-tracker/raw/master/screenshot.png)

=================
See:

https://www.openstreetmap.org/

https://bk.gnarf.org/creativity/bigbrothergps/
