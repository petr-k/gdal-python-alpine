# gdal-python-alpine 
![Docker Pulls](https://img.shields.io/docker/pulls/petkr/gdal-python-alpine.svg?style=plastic)


Alpine-based image with Python and [GDAL](http://gdal.org/), compiled with selected additional drivers.

## Included drivers

Some drivers are intentionally disabled to keep the image size on the lower side, while others
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

Output of `gdalinfo --formats` is:

```
Supported Formats:
  VRT -raster- (rw+v): Virtual Raster
  DERIVED -raster- (ro): Derived datasets using VRT pixel functions
  GTiff -raster- (rw+vs): GeoTIFF
  NITF -raster- (rw+vs): National Imagery Transmission Format
  RPFTOC -raster- (rovs): Raster Product Format TOC format
  ECRGTOC -raster- (rovs): ECRG TOC format
  HFA -raster- (rw+v): Erdas Imagine Images (.img)
  SAR_CEOS -raster- (rov): CEOS SAR Image
  CEOS -raster- (rov): CEOS Image
  JAXAPALSAR -raster- (rov): JAXA PALSAR Product Reader (Level 1.1/1.5)
  GFF -raster- (rov): Ground-based SAR Applications Testbed File Format (.gff)
  ELAS -raster- (rw+v): ELAS
  AIG -raster- (rov): Arc/Info Binary Grid
  AAIGrid -raster- (rwv): Arc/Info ASCII Grid
  GRASSASCIIGrid -raster- (rov): GRASS ASCII Grid
  SDTS -raster- (rov): SDTS Raster
  DTED -raster- (rwv): DTED Elevation Raster
  PNG -raster- (rwv): Portable Network Graphics
  JPEG -raster- (rwv): JPEG JFIF
  MEM -raster- (rw+): In Memory Raster
  JDEM -raster- (rov): Japanese DEM (.mem)
  GIF -raster- (rwv): Graphics Interchange Format (.gif)
  BIGGIF -raster- (rov): Graphics Interchange Format (.gif)
  ESAT -raster- (rov): Envisat Image Format
  XPM -raster- (rwv): X11 PixMap Format
  BMP -raster- (rw+v): MS Windows Device Independent Bitmap
  DIMAP -raster- (rov): SPOT DIMAP
  AirSAR -raster- (rov): AirSAR Polarimetric Image
  RS2 -raster- (ros): RadarSat 2 XML Product
  SAFE -raster- (rov): Sentinel-1 SAR SAFE Product
  PCIDSK -raster,vector- (rw+v): PCIDSK Database File
  ILWIS -raster- (rw+v): ILWIS Raster Map
  SGI -raster- (rw+): SGI Image File Format 1.0
  SRTMHGT -raster- (rwv): SRTMHGT File Format
  Leveller -raster- (rw+): Leveller heightfield
  Terragen -raster- (rw+): Terragen heightfield
  ISIS3 -raster- (rw+v): USGS Astrogeology ISIS cube (Version 3)
  ISIS2 -raster- (rw+v): USGS Astrogeology ISIS cube (Version 2)
  PDS -raster- (rov): NASA Planetary Data System
  VICAR -raster- (rov): MIPL VICAR file
  TIL -raster- (rov): EarthWatch .TIL
  ERS -raster- (rw+v): ERMapper .ers Labelled
  L1B -raster- (rovs): NOAA Polar Orbiter Level 1b Data Set
  FIT -raster- (rwv): FIT Image
  RMF -raster- (rw+v): Raster Matrix Format
  MSGN -raster- (ro): EUMETSAT Archive native (.nat)
  RST -raster- (rw+v): Idrisi Raster A.1
  INGR -raster- (rw+v): Intergraph Raster
  GSAG -raster- (rwv): Golden Software ASCII Grid (.grd)
  GSBG -raster- (rw+v): Golden Software Binary Grid (.grd)
  GS7BG -raster- (rw+v): Golden Software 7 Binary Grid (.grd)
  COSAR -raster- (rov): COSAR Annotated Binary Matrix (TerraSAR-X)
  TSX -raster- (rov): TerraSAR-X Product
  COASP -raster- (ro): DRDC COASP SAR Processor Raster
  R -raster- (rwv): R Object Data Store
  MAP -raster- (rov): OziExplorer .MAP
  KMLSUPEROVERLAY -raster- (rwv): Kml Super Overlay
  PDF -raster,vector- (w+): Geospatial PDF
  CALS -raster- (rw): CALS (Type 1)
  SENTINEL2 -raster- (rovs): Sentinel 2
  PNM -raster- (rw+v): Portable Pixmap Format (netpbm)
  DOQ1 -raster- (rov): USGS DOQ (Old Style)
  DOQ2 -raster- (rov): USGS DOQ (New Style)
  GenBin -raster- (rov): Generic Binary (.hdr Labelled)
  PAux -raster- (rw+): PCI .aux Labelled
  MFF -raster- (rw+v): Vexcel MFF Raster
  MFF2 -raster- (rw+): Vexcel MFF2 (HKV) Raster
  FujiBAS -raster- (ro): Fuji BAS Scanner Image
  GSC -raster- (rov): GSC Geogrid
  FAST -raster- (rov): EOSAT FAST Format
  BT -raster- (rw+v): VTP .bt (Binary Terrain) 1.3 Format
  LAN -raster- (rw+v): Erdas .LAN/.GIS
  CPG -raster- (ro): Convair PolGASP
  IDA -raster- (rw+v): Image Data and Analysis
  NDF -raster- (rov): NLAPS Data Format
  EIR -raster- (rov): Erdas Imagine Raw
  DIPEx -raster- (rov): DIPEx
  LCP -raster- (rwv): FARSITE v.4 Landscape File (.lcp)
  GTX -raster- (rw+v): NOAA Vertical Datum .GTX
  LOSLAS -raster- (rov): NADCON .los/.las Datum Grid Shift
  NTv2 -raster- (rw+vs): NTv2 Datum Grid Shift
  CTable2 -raster- (rw+v): CTable2 Datum Grid Shift
  ACE2 -raster- (rov): ACE2
  SNODAS -raster- (rov): Snow Data Assimilation System
  KRO -raster- (rw+v): KOLOR Raw
  ROI_PAC -raster- (rw+v): ROI_PAC raster
  RRASTER -raster- (rov): R Raster
  ENVI -raster- (rw+v): ENVI .hdr Labelled
  EHdr -raster- (rw+v): ESRI .hdr Labelled
  ISCE -raster- (rw+v): ISCE raster
  ARG -raster- (rwv): Azavea Raster Grid format
  RIK -raster- (rov): Swedish Grid RIK (.rik)
  USGSDEM -raster- (rwv): USGS Optional ASCII DEM (and CDED)
  GXF -raster- (ro): GeoSoft Grid Exchange Format
  NWT_GRD -raster- (rw+v): Northwood Numeric Grid Format .grd/.tab
  NWT_GRC -raster- (rov): Northwood Classified Grid Format .grc/.tab
  ADRG -raster- (rw+vs): ARC Digitized Raster Graphics
  SRP -raster- (rovs): Standard Raster Product (ASRP/USRP)
  BLX -raster- (rwv): Magellan topo (.blx)
  SAGA -raster- (rw+v): SAGA GIS Binary Grid (.sdat)
  XYZ -raster- (rwv): ASCII Gridded XYZ
  HF2 -raster- (rwv): HF2/HFZ heightfield raster
  OZI -raster- (rov): OziExplorer Image File
  CTG -raster- (rov): USGS LULC Composite Theme Grid
  E00GRID -raster- (rov): Arc/Info Export E00 GRID
  ZMap -raster- (rwv): ZMap Plus Grid
  NGSGEOID -raster- (rov): NOAA NGS Geoid Height Grids
  IRIS -raster- (rov): IRIS data (.PPI, .CAPPi etc)
  PRF -raster- (rov): Racurs PHOTOMOD PRF
  CAD -raster,vector- (rovs): AutoCAD Driver 
```

## License

Copyright © 2018, [Petr Krebs](https://github.com/petr-k).
Released under the [MIT License](LICENSE).

***
