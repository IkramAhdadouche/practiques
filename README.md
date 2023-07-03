# practiques


https://common.recitty.com/geoserver/manlleu/wms?&FEATURE_COUNT=50000&viewparams=date_observacions:11042023&SERVICE=WMS&VERSION=1.1.0&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&LAYERS=waste_vehicles_routes_muni_t&SRS=EPSG%3A3857&STYLES=&WIDTH=1921&HEIGHT=1031&BBOX=249627.5259108224%2C5158185.100119142%2C262334.13363258756%2C5165004.731853208


https://common.recitty.com/geoserver/manlleu/wms?VERSION=1.1.0&FORMAT=image%2Fpng&TRANSPARENT=true


https://common.recitty.com/geoserver/manlleu/wfs?VERSION=1.1.0&FORMAT=image%2Fpng


public concatUrlWms():string{
        // retorna la url de wms amb tots els paramentres concatenats.
        let result_url;
       
        let url_wms=this.config.urlWms;
        let params_version=this.config.paramsWmsVersion;
        let params_format= this.config.paramsWmsFormat;
        let params_transparent = this.config.paramsWmsTransparent;

        return result_url= url_wms+'VERSION'+params_version+'&FORMAT='+params_format+'&TRANSPARENT='+params_transparent;
        

    }


    public concatUrlWfs():string{

        let result_url;

        let url_wfs=this.config.urlWfs;
        let params_version=this.config.paramsWfsVersion;
        let output_format=this.config.paramsWfsOutputFormat;

        return result_url= url_wfs+'VERSION'+params_version+'&FORMAT='+output_format;


    }
