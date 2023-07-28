

 public layerIdExists(layer_id:string):boolean{
        const cards = this.getCards();
        if(cards.find((card)=> card.layer_id === layer_id)){
            return true;
        }
        else return false;
    }

    public getCardInformation(layer_id:string):any[] | string{
        if (this.layerIdExists(layer_id)){
            return this.appConfig.cardInformation;
        }
        else{
            return "There's no card information for layer id " +layer_id;
        }

    }

    public getFieldInformation(layer_id:string):any[]|string{
        if(this.layerIdExists(layer_id)){
            return this.appConfig.fields;
        }
        else{
            return "There's no field information for layer id " + layer_id;
        }
    }
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
