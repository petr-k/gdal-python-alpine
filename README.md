# gdal-python-alpine

Alpine-based image with Python and [GDAL](http://gdal.org/), compiled with selected additional drivers.

## Included drivers

Some drivers are intentionally disabled to keep the image size down, while others
(namely [LIBKML](http://www.gdal.org/drv_libkml.html)) are specifically included.

Output of `ogrinfo --formats` is:

```
Supported Formats:
  PCIDSK -raster,vector- (rw+v): PCIDSK Database File
  PDF -raster,vector- (w+): Geospatial PDF
  ESRI Shapefile -vector- (rw+v): ESRI Shapefile
  MapInfo File -vector- (rw+v): MapInfo File
  UK .NTF -vector- (ro): UK .NTF
  OGR_SDTS -vector- (ro): SDTS
  S57 -vector- (rw+v): IHO S-57 (ENC)
  DGN -vector- (rw+): Microstation DGN
  OGR_VRT -vector- (rov): VRT - Virtual Datasource
  REC -vector- (ro): EPIInfo .REC 
  Memory -vector- (rw+): Memory
  BNA -vector- (rw+v): Atlas BNA
  CSV -vector- (rw+v): Comma Separated Value (.csv)
  GML -vector- (rw+v): Geography Markup Language (GML)
  GPX -vector- (rw+v): GPX
  LIBKML -vector- (rw+v): Keyhole Markup Language (LIBKML)
  KML -vector- (rw+v): Keyhole Markup Language (KML)
  GeoJSON -vector- (rw+v): GeoJSON
  OGR_GMT -vector- (rw+): GMT ASCII Vectors (.gmt)
  WAsP -vector- (rw+v): WAsP .map format
  OpenFileGDB -vector- (rov): ESRI FileGDB
  XPlane -vector- (rov): X-Plane/Flightgear aeronautical data
  DXF -vector- (rw+v): AutoCAD DXF
  CAD -raster,vector- (rovs): AutoCAD Driver
  Geoconcept -vector- (rw+): Geoconcept
  GeoRSS -vector- (rw+v): GeoRSS
  GPSTrackMaker -vector- (rw+v): GPSTrackMaker
  PGDUMP -vector- (w+v): PostgreSQL SQL dump
  GPSBabel -vector- (rw+): GPSBabel
  SUA -vector- (rov): Tim Newport-Peace's Special Use Airspace Format
  OpenAir -vector- (rov): OpenAir
  OGR_PDS -vector- (rov): Planetary Data Systems TABLE
  HTF -vector- (rov): Hydrographic Transfer Vector
  AeronavFAA -vector- (rov): Aeronav FAA
  EDIGEO -vector- (rov): French EDIGEO exchange format
  SVG -vector- (rov): Scalable Vector Graphics
  Idrisi -vector- (rov): Idrisi Vector (.vct)
  ARCGEN -vector- (rov): Arc/Info Generate
  SEGUKOOA -vector- (rov): SEG-P1 / UKOOA P1/90
  SEGY -vector- (rov): SEG-Y
  ODS -vector- (rw+v): Open Document/ LibreOffice / OpenOffice Spreadsheet 
  XLSX -vector- (rw+v): MS Office Open XML spreadsheet
  SXF -vector- (ro): Storage and eXchange Format
  Selafin -vector- (rw+v): Selafin
  JML -vector- (rw+v): OpenJUMP JML
  VDV -vector- (rw+v): VDV-451/VDV-452/INTREST Data Format
  TIGER -vector- (rw+v): U.S. Census TIGER/Line
  AVCBin -vector- (ro): Arc/Info Binary Coverage
  AVCE00 -vector- (ro): Arc/Info E00 (ASCII) Coverage
```