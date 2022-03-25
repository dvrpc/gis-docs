# About

DVRPC’s legacy enterprise GIS consisted of an ArcGIS server and an Oracle geodatabase with our planners using ArcGIS desktop and our web applications using services hosted on our ArcGIS server.  While the system worked well, there were some drawbacks with things like database management flexibility, license access for desktop users, and ArcGIS server flexibility.  ESRI’s software and services have since evolved to products like ArcGIS Portal/Online to provide a more powerful ‘online’ foundation for mapping, data management, and web GIS within the enterprise.  These products will help shape DVRPC’s GIS future and make GIS more accessible and easier for all to use.

DVRPC’s new Enterprise GIS Deployment consists of six main components

* [ArcGIS Enterprise Portal](https://arcgis.dvrpc.org/dvrpc/home) plays a central role in organizing and sharing GIS data within our ArcGIS system. The portal provides a user-friendly, searchable repository for our data. It also helps staff view data and create and share maps.  Most of the GIS data in these maps originates from our Enterprise Geodatabase and is hosted by our ArcGIS server. The portal provides an easy window into our GIS data library without requiring heavy GIS software training or ArcGIS Desktop licenses.  All staff can login with their Windows domain login and password and can view data, even from outside of DVRPC’s network.

* [ArcGIS Server](https://arcgis.dvrpc.org/portal) is our hosting server that powers mapping and analysis in our Portal

* [PostgreSQL Database](https://www.postgresql.org/about/) stores all geospatial data and is registered as a data store with ArcGIS Server. Data is compatible/accessible with ESRI software and open source software/languages like QGIS, R, SQL, Python, and many more

* [ArcGIS Web Adaptor](https://enterprise.arcgis.com/en/server/latest/install/windows/about-the-arcgis-web-adaptor.htm) integrates ArcGIS Server and Portal with our existing web servers and our organization's security infrastructure.

* [ArcGIS Data Store](https://enterprise.arcgis.com/en/portal/latest/administer/windows/what-is-arcgis-data-store.htm) provides nimble data storage for the hosting server used with our deployment.  There are no plans right now to use the data store, but it’s software is installed and configured to work with the Server/Portal.

* [ArcGIS Online](https://www.esri.com/en-us/arcgis/products/arcgis-online/overview) is a cloud-based product to make maps, share and collaborate with the public and member governments through apps and open data initiatives.