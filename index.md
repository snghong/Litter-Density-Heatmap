## Welcome to AI Trash Detection Heatmap
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>AI Trash Detection Heatmap</title>
    <link rel="stylesheet" href="static/style.css">
  </head>
  <body>
    <div>
      <h1 id="title">Welcome to the Trash Heatmap of Pittsburgh!
      </h1>
    </div>
    <div id="map"></div>
    
    <script>
      var map, heatmap;

      function initMap() {
        var heatMapData = [
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 0.5},
          new google.maps.LatLng(40.445261, -80.34025),
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 2},
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 3},
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 2},
          new google.maps.LatLng(40.445261, -80.34025),
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 0.5},

          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 3},
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 2},
          new google.maps.LatLng(40.445261, -80.34025),
          {location: new google.maps.LatLng(40.445261, -80.34025), weight: 0.5},
          new google.maps.LatLng(40.445261, -80.34025),
          {location: new google.maps.LatLng(40.785, -80.440), weight: 2},
          {location: new google.maps.LatLng(40.0, -80.435), weight: 3}
        ];
        
        var pittsburgh = new google.maps.LatLng(41, -79.94025);
        map = new google.maps.Map(document.getElementById('map'), {
          center: pittsburgh,
          zoom: 13,
          mapTypeId: 'roadmap'
        });
        
        var heatmap = new google.maps.visualization.HeatmapLayer({
          data: heatMapData
        });
        heatmap.setMap(map);
        }

    </script>
    <script async defer src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAQoa_n2NLmjVJE2trXM8Ca73QI9peFyKA&libraries=visualization&callback=initMap">
    </script>
  </body>
</html>
