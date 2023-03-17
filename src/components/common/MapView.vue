<template>
    <div id="mapview">
    </div>
  </template>

  <script>
import { loadModules } from 'esri-loader';
const options = {
  url:'https://js.arcgis.com/4.26/',
  css:'https://js.arcgis.com/4.26/esri/themes/light/main.css',
};

  export default {
    name: 'MapView',
    components: {},
    mounted: function() {
      this._createMapView();
    },
    methods: {
      async _createMapView() {
        const [Map,MapView] = await loadModules(
          ['esri/Map','esri/views/MapView'],
          options
        );
        const map = new Map({
          basemap:'osm',
        });
        const view = new MapView({
          container:'mapview',
          map:map,
          zoom:10,
          center:[114.35,30.69],
        });

        view.ui.components = [];
        console.log(view);
      },
    },
  };
  </script>
  
  <style>
  #mapview {
    position: relative;
    width: 100%;
    height: 100%;
  }
  </style>
  