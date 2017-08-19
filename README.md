Sharp Turns Onto Ramps
======================

[daniel-j-h](http://www.openstreetmap.org/user/daniel-j-h) wrote up a great
OSM diary entry on the problem of
[Sharp Turns onto Ramps](http://www.openstreetmap.org/user/daniel-j-h/diary/41777)
and how they are handling by routing software. Basically, if there is both a south-bound
entrance to a freeway along with a north-bound entrance, if you fail to take the entrance
to one, the routing software might recalculate and tell you to take the second entrance
if there aren't proper turn restrictions set at that node. This could result in
instructions to take a dangerous turn that is against local traffic laws.

Daniel and the OSRM team have been working on a feature to validate those improper
sharp turns and are dumping out a list of nodes that look to be a problem. He put out a call
to the community to help clean up the data and published a couple of maps with nodes. I
am taking his code and trying to generate smaller data sets (since that's all my computer
can handle) on a more frequent basis.

Maps
----
Maps can be found in the `maps` directory and roughly correlate to the layout of the
partial maps on [Geofabrik](http://download.geofabrik.de/). I'll attempt to include
metadata about the map in the commit messages going forward. Mostly, the date of the
map, and anything else that might be useful.

Exceptions
----------
If you find that some nodes are being called out as too sharp, but they are valid as mapped
and you don't want to see them on future maps, you can edit the `exceptions.json` file and
submit a pull request and they'll be eliminated from future maps.

Requests
--------
If you have a request for a particular country/state/region, let me know and I'll add it
to my list of maps to generate manually until I can determine if there is a greater need
for automated generation of the entire planet.
