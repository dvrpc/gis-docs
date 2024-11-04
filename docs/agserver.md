## ArcGIS Server Configuration

DVRPC followed a pretty standard installation and configuration procedure for our ArcGIS Server.  Initial configuration can be found on `gis-server` at `C:\serverconfig\serverconfig.xml`  

ESRI documentation for ArcGIS server installation can be found [here](https://enterprise.arcgis.com/en/server/latest/install/windows/welcome-to-the-arcgis-for-server-install-guide.htm)

Our ArcGIS Server is federated with our ArcGIS Portal.  Federating an ArcGIS Server site with your Portal integrates the security and sharing models of your Portal with the ArcGIS Server site.

---
### Backup and Recovery

DVRPC uses the standard [ESRI backup utility](https://enterprise.arcgis.com/en/server/latest/develop/windows/backup-utility.htm) for our ArcGIS server on an infrequent basis.  The only downfall to using this utility though is that it doesn't backup cache tiles and tiling schemes.  It's possible to modify the backup script to accommodate the cache located at `C:\arcgisserver\directories\arcgiscache`

[Backup and Recovery scripts](https://github.com/dvrpc/gis-admin/tree/main/agserver)
