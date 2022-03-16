## Software versions and details of configuration

* Windows Server 2019 Standard on all servers

* `gis-db` PostgreSQL 11.2, POSTGIS 2.5.1 
(Esri support begins with ArcGIS 10.7.1 and ArcGIS Pro 2.4)
Using PostGIS Geometry type
User Schema (biota, freight, demographics, transportation, etc.)

* `gis-server` ArcGIS Server 10.9
Federated server
https://gis-server.dvrpc.org/arcgis (internal address)
https://arcgis.dvrpc.org/portal (external address)
Registered data stores (PostgreSQL data owner connection files, ArcGIS data store)
IIS

* `gis-portal` ArcGIS Portal 10.9
https://gis-portal.dvrpc.org/arcgis/home/ (internal address)
https://arcgis.dvrpc.org/dvrpc/home (external address)
Windows Authentication
IIS

* `gis-db` ArcGIS Data Store 10.9
* `web-06` ArcGIS Web Adaptor 10.9