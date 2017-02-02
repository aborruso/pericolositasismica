# Pericolosità sismica di riferimento a passo 0,02 gradi

Questo repo è stato creato per rendere disponibile un archivio di tiles del layer **Pericolosità sismica di riferimento a passo 0,02 gradi** disponibile nel [Portale Cartografico Nazionale](http://www.pcn.minambiente.it/geoportal/catalog/search/resource/details.page?uuid=%7BDC542424-6C37-4B40-9A17-A7B72402D2F1%7D)

La licenza è [Creative Commons Attribuzione - Condividi allo stesso modo 3.0 Italia](http://creativecommons.org/licenses/by-sa/3.0/it)

## tools

Generato con [gdal2tiles](http://www.gdal.org/gdal2tiles.html) con la seguente stringa:

    gdal2tiles -z 1-11 --profile=mercator source.txt

Il file source (in formato [GDAL WMS](http://www.gdal.org/frmt_wms.html)) è così fatto:

```XML
<GDAL_WMS> 
    <Service name="WMS"> 
	<Version>1.1.1</Version> 
	<Transparent>TRUE</Transparent>
	<ServerUrl>http://wms.pcn.minambiente.it/ogc?map=/ms_ogc/WMS_v1.3/Vettoriali/Pericolosita_sismica_002.map</ServerUrl> 
	<SRS>EPSG:4326</SRS> 
        <ImageFormat>image/png</ImageFormat> 
        <Layers>RN.PERICOLOSITA_SISMICA_002GRADI</Layers> 
        <Styles></Styles> 
    </Service> 
    <DataWindow> 
        <UpperLeftX>6</UpperLeftX> 
        <UpperLeftY>49</UpperLeftY> 
        <LowerRightX>18.92</LowerRightX> 
        <LowerRightY>34.5</LowerRightY> 
        <SizeX>19380</SizeX> 
        <SizeY>21750</SizeY> 
    </DataWindow> 
    <Timeout>3000</Timeout>
	<MaxConnections>1</MaxConnections>
    <Projection>EPSG:4326</Projection>
	<BandsCount>4</BandsCount>
</GDAL_WMS>
```
	

