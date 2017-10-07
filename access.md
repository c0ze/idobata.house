---
layout: page
title: "アクセス"
date: 2014-10-05 15:42
---


  <div id="map-container" height="300px"></div>
  <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>
  <script src="http://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.1.1/js/bootstrap.min.js"></script>
  <script async defer
    src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAIg6b5ODnU_HpwrUvj_Di2uV3HqDwBKNw&callback=initMap&sensor=false">
  </script>

  <script type="text/javascript">
    var initMap = function () {
      var_location = new google.maps.LatLng(35.662470, 139.628358);
      var_mapoptions = {
        center: var_location,
        zoom: 15
      };
	  var_map = new google.maps.Map(document.getElementById("map-container"), var_mapoptions);
      var_marker = new google.maps.Marker({
        position: var_location,
        map: var_map,
        title:"井戸端マザーハウス"});
      document.getElementById("map-container").style.height="500px";
      var_marker.setMap(var_map);
	}
    google.maps.event.addDomListener(window, 'load', initMap);
	</script>
