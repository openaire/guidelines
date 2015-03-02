.. _d:geolocation:

18. GeoLocation (O)
-------------------

Spatial region or named place where the data was gathered or about which the data is focused (occurrences: 0-n).

**Allowed values, examples, other constraints**

Repeat this property to indicate several different locations.

.. _d:geolocationpoint:

18.1 geoLocationPoint (O)
~~~~~~~~~~~~~~~~~~~~~~~~~

A point location in space (occurrences: 0-1).

**Allowed values, examples, other constraints**

A point contains a single latitude‐longitude pair, separated by whitespace.

See :ref:`d:geolocation_instructions`.

.. _d:geolocationbox:

18.2 geoLocationBox (O)
~~~~~~~~~~~~~~~~~~~~~~~

The spatial limits of a place (occurrences: 0-1).

**Allowed values, examples, other constraints**

A box contains two white space separated latitude‐longitude pairs, with each pair separated by whitespace. The first pair is the lower corner (normally south west), the second is the upper corner (normally north east).

See :ref:`d:geolocation_instructions`.

.. _d:geolocationplace:

18.3 geoLocationPlace (O)
~~~~~~~~~~~~~~~~~~~~~~~~~

Description of a geographic location (occurrences: 0-1).

**Allowed values, examples, other constraints**

Free text. Use to describe a geographic location.

.. _d:geolocation_instructions:

Detailed usage instructions
~~~~~~~~~~~~~~~~~~~~~~~~~~~
Use WGS 84 (World Geodetic System) coordinates. Use only decimal numbers for coordinates. Longitudes are ‐180 to 180 (0 is Greenwich, negative numbers are west, positive numbers are east), Latitudes are ‐90 to 90 (0 is the equator; negative numbers are south, positive numbers north).


Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <geoLocations>
     <geoLocation>
       <geoLocationPoint>31.233 -67.302</geoLocationPoint>
       <geoLocationBox>41.090 -71.032 42.893 -68.211</geoLocationBox>
       <geoLocationPlace>Atlantic Ocean</geoLocationPlace>
     </geoLocation>
   </geoLocations>
