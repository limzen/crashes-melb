<!DOCTYPE HTML>

<!-- This HTML file is produced for Assignment 2, GEOM90007 -->
<!-- Mingzhe LI 930163 -->
<!-- 24 Sep 2019 -->

<html lang="en">
<head>
<meta charset='utf-8' />
<script src='https://api.mapbox.com/mapbox-gl-js/v0.48.0/mapbox-gl.js'></script>
<link href='https://api.mapbox.com/mapbox-gl-js/v0.48.0/mapbox-gl.css' rel='stylesheet' />
<style>
  
body {
  margin: 0;
  padding: 0;
}

#map {
  position: absolute;
  top: 0;
  bottom: 0;
  width: 100%;
}

/* Add the map ovelay style */
.map-overlay {
  position: absolute;
  font: 12px/20px 'Helvetica Neue', Arial, Helvetica, sans-serif;
  overflow: auto;
  opacity: 0.9;
  color: #ddd;
  width: 20%;
  border-radius: 8px;
  padding: 10px;
}

/* Add the map ovelay inner style */
.map-overlay .map-overlay-inner {
  background: #17171d;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  padding: 10px 20px;
  margin-bottom: 10px;
}

/* Add the map ovelay inner - legend style */
#legend {
  bottom: 2%;
  left: 10px;
  width: 18%;
  background: #17171d;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
  margin-bottom: 10px;
}
  
h1 {
  font-size: 19px;
  line-height: 15px;
}

h2 {
  font-size: 13px;
  line-height: 10px;
  margin-bottom: 12px;
}

a {
  text-decoration: none;
  color: #2dc4b2;
}

.session {
  margin-bottom: 15px;
}

.row {
  width: 90%;
  height: 25px;
  opacity: 0.7;
  transition: 0.2s;
}

.colors_heatmap {
  background: linear-gradient(to right, #fef0d9, #fdcc8a, #fc8d59, #e34a33, #b30000);
  margin-bottom: 5px;
}

.colors_totperson {
  background: linear-gradient(to right, #fef0d9, #fdcc8a, #fc8d59, #e34a33, #b30000);
  margin-bottom: 5px;
}

.colors_choro {
  background: linear-gradient(to right, #2c7bb6, #abd9e9, #ffffbf, #fdae61, #d7191c);
  margin-bottom: 5px;
}

.label {
  width: 18%;
  display: inline-block;
  text-align: center;
}

.mapboxgl-popup-content {
  font: 12px/20px 'Helvetica Neue', Arial, Helvetica, sans-serif;
  color: #aa5e79;
  background-color: white;
  border-color: #91785D;
  max-width: 180px;
  box-shadow: 3px 3px 2px #aa5e79;
  opacity: 0.9;
}
</style>

</head>

<body>
<meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.48.0/mapbox-gl.js'></script> 
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.48.0/mapbox-gl.css' rel='stylesheet' />

<!-- add map div -->
<div id='map'></div>

<div class='map-overlay' id='title'>
  <div class='map-overlay-inner'>
    <h1>Crashes in Melbourne</h1> 
    <p>Data: <a href='https://discover.data.vic.gov.au/dataset/crashes-last-five-years'>public dataset of crashes </a> in last five years in Melbourne from VicRoads</p>
    
    <div class='session' id='sliderbar'>   
      <h2><label id='choro-label'>Year Peroid: 2013 - 2014</label>
      <label id='heatmap-label' style='display: none;'>Financial Year: 2013</label></h2>

      <h2> <input id='slider' class='row' type='range' min='13' max='16' step='1' value='13' />
      <input id='slider_heatmap' class='row' type='range' min='2013' max='2019' step='1' value='2013' style='display: none;'/> </h2>
      <h2>Select map types</h2>
      <div class='row' id='filters'>
        <input id='heatmap' type='radio' name='toggle' value='crash_heatmap'>
        <label for='heatmap'>Heatmap & Dot Map</label>
        <input id='choro' type='radio' name='toggle' value='Crash_change'>
        <label for='choro'>Choropleth Map</label>
      </div>
    </div>
  </div>     
</div>

<div class='map-overlay' id='legend'>
  <div id='heatmap_legend' class='session' style='display: none;'>
    <h2>Crash Heatmap Density</h2> 
    <div class='row colors_heatmap'></div> 
    <div class='row labels'>
      <div class='label'>0.2</div>
      <div class='label'>0.4</div>
      <div class='label'>0.6</div>
      <div class='label'>0.8</div>
      <div class='label'>1.0</div>
    </div>
  </div>

  <div id='circle_legend' class='session' style='display: none;'>
    <h2>Total Persons in Crash</h2>
    <div class='row colors_totperson'></div>
    <div class='row labels'>
      <div class='label'>1</div>
      <div class='label'>3</div>
      <div class='label'>5</div>
      <div class='label'>10</div>
      <div class='label'>20+</div>
    </div>
  </div>
 
  <div id='choro_legend' class='session'>
    <h2>Carsh Count Change Rate</h2> 
    <div class='row colors_choro'></div> 
    <div class='row labels'>
      <div class='label'>-10%</div>
      <div class='label'>-5%</div>
      <div class='label'>0</div>
      <div class='label'>5%</div>
      <div class='label'>10%</div>
    </div>
  </div>
  
</div>
<script>

// Check browser	
if (!('fetch' in window)) {
      alert('Sorry, your browser is not supported. Recommended browsers are Chrome, Firefox, and Safari.');
      throw new Error('unsupported browser');
    }

// Mapbox accessToken 
mapboxgl.accessToken = 'pk.eyJ1IjoibWluZ3poZWwiLCJhIjoiY2p6dDVlaG16MDF0NTNhb2Vld2JkdnJ6NiJ9.rWzkEJWYiZ3D-fEqj95ruQ';

// Mapbox map style URL
var map = new mapboxgl.Map({
  container: 'map',
  style: 'mapbox://styles/mapbox/dark-v10',
  center: [145,-37.9],
  zoom: 9.3
});

// Add zoom and rotation controls to the map.
map.addControl(new mapboxgl.NavigationControl());


// Add the 'if the map is on and loaded' function:
map.on('load', function () {

	var layers = map.getStyle().layers;
		// Find the index of the first symbol layer in the map style
        var firstSymbolId;
        for (var i = 0; i < layers.length; i++) {
          if (layers[i].type === 'symbol') {
            firstSymbolId = layers[i].id;
            break;
				}
		}
   
  // Add the heatmap layer
  map.addLayer({
    
    id: "crash_heatmap",
    layout: {
      'visibility':'none'
    },
      type: 'heatmap',
      source: {
        'type': 'vector',
        'url': 'mapbox://mingzhel.8dektpgh'
    },
      'source-layer': 'crashes-7ubx0z',
      paint: {
      // increase weight as diameter breast height increases
      'heatmap-weight': {
        property: 'TOTAL_PERS',
        type: 'exponential',
        stops: [
          [1, 0],
          [54, 1]
        ]
      }, 
       // increase intensity as zoom level increases
      'heatmap-intensity': {
        stops: [
          [11, 1],
          [15, 3]
        ]
      },    
 	 'heatmap-color': [
        'interpolate',
        ['linear'],
        ['heatmap-density'],
        0, 'rgba(236,222,239,0)',
        0.2, '#fdcc8a',
        0.4, '#fc8d59',
        0.6, '#fc8d59',
        0.8, '#e34a33'],
     // increase radius as zoom increases
    'heatmap-radius': {
      stops: [
        [11, 15],
        [15, 20]
      ]},
    // decrease opacity to transition into the circle layer
    'heatmap-opacity': {
      default: 1,
      stops: [
        [12, 1],
        [12.5, 0]
        ]}
    }
  }, firstSymbolId);
  
  // add the proportional symbol layer
  map.addLayer({
    id: 'crash_circle',
    type: 'circle',
    layout: {
      'visibility':'none'
    },
    source: {
        'type': 'vector',
        'url': 'mapbox://mingzhel.8dektpgh'
    },
    'source-layer': 'crashes-7ubx0z',
    minzoom: 12,
    paint: {
      // increase the radius of the circle as the zoom level and person count value increases
      'circle-radius': {
        property: 'TOTAL_PERS',
        type: 'exponential',
        stops: [
          [{ zoom: 15, value: 1 }, 5],
          [{ zoom: 15, value: 54 }, 10],
          [{ zoom: 22, value: 1 }, 20],
          [{ zoom: 22, value: 54 }, 50],
        ]
      },
      'circle-color': {
        property: 'TOTAL_PERS',
        type: 'exponential',
        stops: [
          [1, '#fef0d9'],
          [3, '#fdcc8a'],
          [5, '#fc8d59'],
          [10, '#e34a33'],
          [20, '#b30000']
        ]
      },
      'circle-stroke-color': 'white',
      'circle-stroke-width': 1,
      'circle-opacity': {
        stops: [
          [11, 0],
          [12.5, 1]
        ]
      }
    }
  });
  
  //init map filter as 2013
  map.setFilter('crash_heatmap', ['==', ['number', ['get', 'ACC_YEAR']], 2013]);
  map.setFilter('crash_circle', ['==', ['number', ['get', 'ACC_YEAR']], 2013]);
  
  // add the choropleth layer    
  map.addLayer({
    // the code for which layer and what style goes i	n here
    id: 'Crash_change',
    type: 'fill',
    source: {
      type: 'vector',
      url: 'mapbox://mingzhel.71yfu3yi'
    },
    'source-layer': 'melb_data-bu95d8',
    'paint': {
      'fill-color': {
        property: "D_13_14",
        type: 'interval',
        default: '#D3D3D3',
        stops: [
          [-0.1, '#2c7bb6'],
          [-0.05, '#abd9e9'],
          [0, '#ffffbf'],
          [0.05, '#fdae61'],
          [0.1, '#d7191c']
        ]
      },
      'fill-opacity': 0.7,
      'fill-outline-color': '#888888'
    }
  }, firstSymbolId);
    
  // get the input element to swtich layer  
  document.getElementById('slider').addEventListener('input', function(e) {
  	
    var year = parseInt(e.target.value);
    var year_2 = year + 1;
    var year_period = "D_" + year.toString() + "_" + year_2.toString();
    
  
    var year_name = "Year Period: 20" + year + " - " + "20" + year_2; 	
    document.getElementById('choro-label').innerText = year_name; 
    // add 'click pop-up show info' function
    map.on('click', 'Crash_change', function(e) {
      new mapboxgl.Popup()
        .setLngLat(e.lngLat)
        .setHTML(e.features[0].properties.SA3_NAME16 + "<br />" +
                 year_name + "<br />" +
                 "Change rate: " +  Math.round(e.features[0].properties[year_period]*100) + "%")
        .addTo(map);
    });

    map.setPaintProperty('Crash_change', 'fill-color' , {
      property: year_period,
      type: 'interval',
      default: '#D3D3D3',
      stops: [
        [-0.1, '#2c7bb6'],
        [-0.05, '#abd9e9'],
        [0, '#ffffbf'],
        [0.05, '#fdae61'],
        [0.1, '#d7191c']
      ]
    });

  });
  
  // init text content and time slider to choropleth map 
  map.on('click', 'Crash_change', function(e) {
    new mapboxgl.Popup()
      .setLngLat(e.lngLat)
      .setHTML(e.features[0].properties.SA3_NAME16 + "<br />" +
               "2013 - 2014 " + "<br />" +
               "Change rate: " +  Math.round(e.features[0].properties.D_13_14*100) + "%")
      .addTo(map);
  });

  // when mouse is over a point change the curse to a pointer
  map.on('mouseenter', 'Crash_change', function() {
    map.getCanvas().style.cursor = 'pointer';
  });

  // Change it back to default map pan cursor
  map.on('mouseleave', 'Crash_change', function() {
    map.getCanvas().style.cursor = '';
  });
  
  // parameters for modify map features
  var heatmap_zoom = document.getElementById('heatmap_legend');
  var heatmap_slider = document.getElementById('slider_heatmap');
  var heatmap_label = document.getElementById('heatmap-label');
  var circle_zoom = document.getElementById('circle_legend');
  var choro_zoom = document.getElementById('choro_legend');
  var choro_slider = document.getElementById('slider');
  var choro_label = document.getElementById('choro-label');
  
  
  // event listener to switch layer  
  document.getElementById('filters').addEventListener('change', function(e) {
    
    var map_type = e.target.value;
    
    // update the map filter
    if (map_type === 'crash_heatmap') {    
    
      choro_zoom.style.display = 'none';
      heatmap_zoom.style.display = 'block';
      
      choro_slider.style.display = 'none';
      choro_label.style.display = 'none';
      choro_legend.style.display = 'none';
      
      heatmap_label.style.display = 'block';
      heatmap_slider.style.display = 'block';
      heatmap_legend.style.display = 'block';
      
      map.on('zoom', function() {
        if (map.getZoom() > 12) {
          heatmap_zoom.style.display = 'none';
          circle_zoom.style.display = 'block';
        } else {
          heatmap_zoom.style.display = 'block';
          circle_zoom.style.display = 'none';
        } 
      });
      
      // hide choropleth map
      map.setLayoutProperty("crash_heatmap", 'visibility', 'visible');
      map.setLayoutProperty("Crash_change", 'visibility', 'none');
      map.setLayoutProperty("crash_circle", 'visibility', 'visible');
      
      document.getElementById('slider_heatmap').addEventListener('input', function(e) {
  	
        var year = parseInt(e.target.value);

        map.setFilter('crash_heatmap', ['==', ['number', ['get', 'ACC_YEAR']], year]);
        map.setFilter('crash_circle', ['==', ['number', ['get', 'ACC_YEAR']], year]);
        
        var yearx = "Finnacial Year: " + year;

        document.getElementById('heatmap-label').innerText = yearx;
      });
          
      map.on('click', 'crash_circle', function(e) {
        new mapboxgl.Popup()
          .setLngLat(e.lngLat)
          .setHTML("LGA Name: " + e.features[0].properties.LGA_NAME + "<br />" +
                   "Accident Date: " + e.features[0].properties.ACCIDENT_D + "<br />" +
                   "Accident Time: " + e.features[0].properties.ACCIDENT_T + "<br />" +
                   "Day of Week: " + e.features[0].properties.DAY_OF_WEE + "<br />" +
                   "Severity Level: " + "<br />" + 
                   e.features[0].properties.SEVERITY + "<br />" +
                   "Total people: " + e.features[0].properties.TOTAL_PERS)
          .addTo(map);
      });

      // when mouse is over a point change the curse to a pointer
      map.on('mouseenter', 'crash_circle', function() {
        map.getCanvas().style.cursor = 'pointer';
      });

      // Change it back to default map pan cursor
      map.on('mouseleave', 'crash_circle', function() {
        map.getCanvas().style.cursor = '';
      });
 
    } else if (map_type === 'Crash_change') {
      
      // update features, to display choropleth map
      choro_zoom.style.display = 'block';
      choro_slider.style.display = 'block';
      choro_label.style.display = 'block';
      choro_legend.style.display = 'block';
      
      heatmap_zoom.style.display = 'none';
      heatmap_legend.style.display = 'none';
      heatmap_label.style.display = 'none';
      heatmap_slider.style.display = 'none';
      
      map.setLayoutProperty("crash_heatmap", 'visibility', 'none');
      map.setLayoutProperty("Crash_change", 'visibility', 'visible');
      map.setLayoutProperty("crash_circle", 'visibility', 'none');
      
    } else {
      console.log('error');
    }
  });
  
});
</script>
</body>
</html>
