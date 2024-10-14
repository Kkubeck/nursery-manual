# Historical Overview of the Nursery

In this section, we explore the development of the nursery over the years.

````{tab-set}
```{tab-item} 2000
Here is the nursery in the year 2000:

```{raw} html
<div id="mapid-2000" style="width: 600px; height: 400px;"></div>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js"></script>

<script>
  var map2000 = L.map('mapid-2000', {
    crs: L.CRS.Simple,
    minZoom: -1,
    maxZoom: 4,
  });

  var bounds = [[0,0], [1000,1000]];
  var image = L.imageOverlay('../images/historical_nursery/2004-03-21.png', bounds).addTo(map2000);
  map2000.fitBounds(bounds);

  // Add markers
  var marker = L.marker([500, 500]).addTo(map2000);
  marker.bindPopup("<b>Planting Area</b><br>Established in 2004.");
</script>


