--
 "layers": {
        "id": "waste_vehicles_routes_muni_t",
        "serviceid": "wms-geoserver",
        "layer": "waste_vehicles_routes_muni_t",
        "opacity": 0.8,
        "title": "waste_vehicles_routes_muni_t",
        "query_layers":["waste_vehicles_routes_muni_t"],
        "order": 4,
        "viewparams": "date_observaciones:",
        "active": false
    },

     public getUrlService(serviceId:string):string | null{
        
        if(!this.config.hasId(serviceId)){
            return null;
        }

        const services = this.config.getServices();
        let index = -1;
        for(let i = 0; i<services.length; i++){ //get service by and id specified
            if(this.config.hasId(services[i].id)){
                index = i;
                break;
            }
        }
        if(index ==-1){
            return null ; // service id not found
        }

        const url = this.config.getUrlByIndex(index);
        const params = this.config.getParamsByIndex(index);

        let urlWithParams = url;
        let serviceParams = '?';
        for(const propertyName in params){
            
            
            /*if(propertyName ==='viewparams'){
               serviceParams += `&${propertyName}=date_observaciones:${this.getCurrentDate()}`;
            }
            else{*/
                serviceParams += `&${propertyName}=${params[propertyName]}`;
            //}
          
        }

        urlWithParams += serviceParams;
        //  urlWithParams += serviceParams + this.layerInformation;
        return urlWithParams;
        
    }


  
