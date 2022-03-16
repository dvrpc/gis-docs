## Implementation

DVRPC has implemented five of these components on four internal virtual machines named:

- `gis-db`: PostgreSQL, ArcGIS Data Store
- `gis-server`: ArcGIS Server (hosting server for Portal, federated), ArcGIS Web Adaptor
- `gis-portal`: ArcGIS Portal, ArcGIS Web Adaptor
- `web-06`: 2 ArcGIS Web Adaptors
    - gis-portal Web Adaptor named 'dvrpc'
    - gis-server Web Adaptor named 'portal'
    - arcgis sub-domain of dvrpc.org

DVRPC will also rely on ESRI’s SAAS cloud product called ArcGIS Online to create web maps, web applications, and promote data sharing with the public. 

DVRPC has registered a large number of public GIS services with ArcGIS Online’s Open Data platform and will continue to use it for open data distribution.

`gis-server`, `gis-portal`, `gis-db` all reside behind the DMZ and are open to the internet with 2 web adaptors installed on `web-06`

ArcGIS Server is federated with ArcGIS Portal and Windows Authentication is active.

![](/images/GIS.png "GIS Enterprise")