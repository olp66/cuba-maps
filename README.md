# cuba-maps
Cuba geojson and topojson maps

The national territory, for the intentions politic and administrative, splits into 15 provinces and in 168 municipalities, including the special municipality of "Isla de la Juventud".

The archives have been created considering the administrative level, feature type and level of detail and show the boundaries of regions.

# name structure

XXX_YYY_ZZZ...Z_AL#_Tf_Dl

XXX: cod of country, CUB for all files
YYY: cod of content, CUB for country maps, cod of province or municipality name
ZZZ...Z: name of subdivisions (optional)
AL#: administrative level, subdivisions of areas/territories recognised by governments for administrative purposes,	 
		admin_level=2 -> national
		admin_level=4 -> province
		admin_level=6 -> municipality
		admin_level=8 -> popular council (Consejo Popular) see note.
Tf: feature type A -> Area / L-> Line
Dl: level of detail, elements content in the map L-low, M-medium, H-high

Examples:

CUB_CUB_AL2_TL_DH.geojson  -> map of country, line feature, high level of detail  	
CUB_ART_AL4_TA_DL.geojson  -> map of Artemisa province, area feature, low level of detail  	
CUB_MTZ_AL6_TA_DL.geojson  -> map of municipalities of Matanzas province, area feature, low level of detail  		
		
Note: The "Consejo Popular" is a local organ of representative character, does not constitute an intermediate request to the intentions of the division politic and administrative, but is used to demarcate the territory inside the municipalities.		

# codification

The files may content this attributes:

srid: province identification 
id: region identification
name: region name
cod: region code
local_name: specific name

The identifications used were stablished by [Resolucion No. 129/2010](http://www.one.cu/resoluciones/2010res129.pdf) of ONEI (National Office of Statistics and Information)

# sources

(https://www.openstreetmap.org/)
(https://osm-boundaries.com/Map)

Maps are verified with maps published on web:

[El Catastro en Puerto Padre Dirección Municipal de Planificación Física Puerto Padre] (https://catastro.cubava.cu)

Self creation.

# simplifications

Some maps have been simplified using TopoJSON [https://github.com/topojson/topojson#topojson] is an extension of GeoJSON that encodes topology. TopoJSON eliminates redundancy, allowing related geometries to be stored efficiently in the same file.


