map.whenReady( () => {

          var arrayMarkers = [];
          var markerBcn = new cercaliagl.Marker({
           
            position: map.setDefaultClick(this.showPopup),
            popup: new cercaliagl.Popup({
              title: 'Barcelona',
              content: 'Barcelona Marker <b>content</b>',
              visible: true,
              offset: [0, -40]
            })
          });
          arrayMarkers.push(markerBcn);
          map.addMarkers(arrayMarkers);


           showPopup(event:MouseEvent):void{
       /* const popup = document.createElement('div');
        popup.className = 'popup';
        popup.textContent = message;
        
        const closeButton = document.createElement('button');
        closeButton.textContent = 'Close';
        closeButton.addEventListener('click',()=> {
          document.body.removeChild(popup);
        });
        popup.appendChild(closeButton);
        document.body.appendChild(popup);*/
        const latitude = event.latLng.lat();
      }
