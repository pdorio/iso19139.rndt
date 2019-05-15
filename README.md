# iso19139.rndt

GeoNetwork Italian RNDT metadata pluggable schema for version 3.x .

- Home site:
  http://www.rndt.gov.it/

- RNDT metadata manuals and technical rules:
  http://geodati.gov.it/geoportale/regole-tecniche-rndt
  

  
  
  This version of plugin was built against a nightly version of Geonetwork 3.4.0, and is used by Provincia Autonoma di Trento (Italy) to publish its metadata italian rules compliants. 
The Provincia Autonoma di Trento has financed the creation of the geonetwork 3.x plugin for the compilation of metadata according to the rndt standard.
The code is donated to the geonetwork community for its public usage.

 The development of this plugin is based on rndt plugin built for Geonetwork 2.x, you can find it  here: https://github.com/geonetwork/schema-plugins
 
## Install the plugin

1. copy the plugin in the geonetwork schemas directory:

```
cp -r iso19139.rndt-master/src/main/plugin/iso19139.rndt geonetwork/WEB-INF/data/config/schema_plugins/. 
```

2. Restart geonetwork

## Configure the plugin

* Remember to change the prefix for UUID. You can simply fix the [line 52 of this file](src/main/plugin/iso19139.rndt/update-fixed-info.xsl#L52) replacing ```p_xx``` with your prefix, eg. ```p_tn```
* If you are using a GeoNetwork 3.4.x version you need to comment the ```appMinorVersionSupported``` tag in the [schema-ident.xml](src/main/plugin/iso19139.rndt/schema-ident.xml#L7) which is not supported by the schema.

## Load models and examples

Simply go to the Admin console -> Metadata & templates, check the RNDT plugin and clic on "Load templates for selected standards"


