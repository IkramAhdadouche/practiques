
"cards": [
        {
            "layer_id": "waste_vehicles_routes_muni_t",
            "card_information": {
                "title": "Titol Fitxa",
                "id": "c1",
                "description": "Aquesta es la descripcio de la fitxa %card_title%"
            },
            "fields": [
                {
                    "field_id": "component_id",
                    "type": "kpi",
                    "min_value": "60",
                    "max_value": "80",
                    "image_url": "./assets/image.png",
                    "link_url": "https://www.nexusgeographics.com/sites/default/files/inline-images/article_cercalia01.png",
                    "text": "Aquest es el text del component sel·leccionat"
                }
            ]
        },         
        {
            "layer_id": "waste_vehicles_routes_muni_t",
            "card_information": {
                "title": "Titol Fitxa",
                "id": "c1",
                "description": "Aquesta es la descripcio de la fitxa %card_title%"
            },
            "fields": [
                {
                    "field_id": "component_id",
                    "type": "kpi",
                    "min_value": "60",
                    "max_value": "80",
                    "image_url": "./assets/image.png",
                    "link_url": "https://www.nexusgeographics.com/sites/default/files/inline-images/article_cercalia01.png",
                    "text": "Aquest es el text del component sel·leccionat"
                }
            ]
        }
    ]

        public getServices():any[]{
        //tots els paramtre de l'array de services (cada parametre de cada posició)
        return this.appConfig.services;
    }

    public getLayers():any[]{
        return this.appConfig.layers;
    }

    public getUrlByIndex(index:number):string | null{
        //a partir d'un index (posicio) retornar la url
        const services = this.getServices();
        if(index >=0 && index <services.length){
            return services[index].url;
        }
        return null; // si no existeix retornar null
    }

    public getParamsByIndex(index:number):any | null {
        //de cada servei obtenir el seus parametres que sera concatenats
        const services = this.getServices();
        if(index>=0 && index < services.length){
            return services[index].params;
        }
        return null; // si no existeix retornar null

    }
