## Database Configuration

The geodatabase is a PostgreSQL database with PostGIS geometry.  The database uses a ‘user-schema’ design.  Only the data owner for each schema can load/edit data.  DVRPC has created a schema for each data category.  Each schema has a data owner user and data viewer user.  An SDE schema houses administrative ESRI SDE tables.  There is also a planner_editor user that was created for versioned editing in any schema.  Installation and configuration of the geodatabase followed [ESRI documentation](https://desktop.arcgis.com/en/arcmap/latest/manage-data/gdbs-in-postgresql/setup-geodatabase-postgresql-windows.htm#) closely.

---
### Schemas and Roles

List of schemas and their respective data owner and viewer user names

- Biota - biota, biota_viewer
- Boundaries - boundaries, boundaries_viewer
- Demographics - demographics, demographics_viewer
- Economy - economy, economy_viewer
- Environment - environment, environment_viewer
- Freight - freight, freight_viewer
- Geology - geology, geology_viewer
- Hydrography - hydrography, hydrography_viewer
- ImgElev - imgelev, imgelev_viewer
- Location - location, location_viewer
- Parcels - parcels, parcels_viewer
- Planning - planning, planning_viewer
- Structure - structure, structure_viewer
- Transportation - transportation, transportation_viewer
- Utilities - utilities, utilites_viewer
- SDE - sde

Other users (dvrpc_viewer, planner_editor, postgres)

`dvrpc_viewer` has read-only permissions on all schemas in the GIS database.  Users can use this role to connect to the database using psql, python, r, QGIS, and other methods to query GIS data.

---
### Backup and Recovery

A backup script runs on gis-db Sundays to ensure optimal data recovery and backups over 30 days are removed.  GIS data is not updated frequently enough to warrant daily backups.

- backup script location on `gis-db`: C:\gis-admin\database\backup\backup.bat
- backups are stored at: \\\filesrv04\GIS_DB$

[backup.bat on Github](https://github.com/dvrpc/gis-admin/blob/main/database/backup/backup.bat)

Recovery can be automated using GIS_DB.py.  This script first runs sql to create the db, create the postgis extension, and create roles/schemas.  Then a bat file is used to restore the db from a backup.  Public schema first, sde schema second, and rest last.  This follows [ESRI best practice](https://desktop.arcgis.com/en/arcmap/latest/manage-data/gdbs-in-postgresql/restore-geodatabase-postgresql.htm) for geodatabase recovery 

[Recovery Scripts on Github](https://github.com/dvrpc/gis-admin/tree/main/database/recovery)
