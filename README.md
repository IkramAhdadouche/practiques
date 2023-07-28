

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
