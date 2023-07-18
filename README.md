
 this.map.setDefaultClick((pixel: any,position: any)=>{
            this.createMarker(position);
          });

createMarker(position:any){
      //createMaker amb position
      var markerBcn = new cercaliagl.Marker({
           
        position: position,
        popup: new cercaliagl.Popup({
          title: 'Barcelona',
          content: 'Barcelona Marker <b>content</b>',
          visible: true,
          offset: [0, -40]
        })
      });

      this.map.addMarkers([markerBcn]);
     }
