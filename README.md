
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
            serviceParams += `&${propertyName}=${params[propertyName]}`;
            
            if(propertyName =='viewparams'){
              
            }
            //data actual ?
        }

        urlWithParams += serviceParams;
        return urlWithParams;
        
    }


    "viewparams":"date_observacions:11042023"
