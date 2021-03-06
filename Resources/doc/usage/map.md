# Map

## Build your map

### By configuration file

By default, the bundle doesn't need any configuration. Most of the service have a default configuration which allows
you to use the given objects like they are. The ``fungio_google_map.map`` service is. The configuration describes
below is this default configuration.

```yaml
# app/config/config.yml

fungio_google_map:
    map:
        # You own map class
        class: "My\Fucking\Map"

        # Your own map helper class
        helper_class: "My\Fucking\MapHelper"

        # Prefix used for the generation of the map javascript variable
        prefix_javascript_variable: "map_"

        # HTML container ID used for the map container
        html_container: "map_canvas"

        # If this flag is enabled, the map will load asynchronous
        async: false

        # If this flag is enabled, the map will autozoom on the overlays added
        auto_zoom: false

        # Center coordinate of the map
        # If the autozoom flag is enabled, the center is not used
        center:
            longitude: 0
            latitude: 0
            no_wrap: true

        # Zoom of the map
        # If the autozoom flag is enabled, the zoom is not used
        zoom: 3

        # Bound of the map
        # If the auto zoom flag is not enabled, the bound is not used
        # If the bound extends overlays, coordinates of the overlays extended are used instead of these coordinates
        # By default, there is no bound
        bound:
            south_west:
                latitude: -2.1
                longitude: -3.9
                no_wrap: true
            north_east:
                latitude: 2.6
                longitude: 1.4
                no_wrap: true

        # Default map type
        # Available map type : hybrid, roadmap, satellite, terrain
        type: "roadmap"

        # Map width
        width: "300px"

        # Map height
        height: "300px"

        # Custom map options
        # By default, there is no map options
        map_options:
            disableDefaultUI: true
            disableDoubleClickZoom: true

        # Custom stylesheet options
        # By default, there is no stylesheet options except width & height
        stylesheet_options:
            border: "1px solid #000"
            background-color: "#fff"

        # google map Api language, default en
        language: en

        # google Api key, (To generate one read: https://console.developers.google.com/flows/enableapi?apiid=maps_backend,geocoding_backend,directions_backend,distance_matrix_backend,elevation_backend,places_backend&keyType=CLIENT_SIDE&reusekey=true)
        api_key: YOUR_API_KEY
```

``` php
<?php

// Requests the fungio google map service
$map = $this->get('fungio_google_map.map');
```

### By coding

If you want to learn more, I recommend you to read
[this documentation](https://github.com/fungio/fungio-google-map/blob/master/doc/usage/map.md).

## Add overlays to your map

Overlays are objects on the map that are tied to latitude/longitude coordinates, so they move when you drag or zoom
the map. Overlays reflect objects that you "add" to the map to designate points, lines, areas, or collections of
objects.

 1. [Marker](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/marker.md)
 2. [Info window](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/info_window.md)
 3. [Polyline](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/polyline.md)
 4. [Encoded Polyline](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/encoded_polyline.md)
 5. [Polygon](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/polygon.md)
 6. [Rectangle](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/rectangle.md)
 7. [Circle](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/circle.md)
 8. [Ground overlay](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/ground_overlay.md)
 9. [Marker cluster](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/overlays/marker_cluster.md)

## Configure map control options

The maps on Google Maps contain UI elements for allowing user interaction through the map. These elements are known as
controls and you can include variations of these controls in your Google Maps API application. Alternatively, you can
do nothing and let the Google Maps API handle all control behavior.

 1. [Map type](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/map_type.md)
 2. [Overview](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/overview.md)
 3. [Pan](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/pan.md)
 4. [Rotate](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/rotate.md)
 5. [Scale](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/scale.md)
 6. [Street view](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/street_view.md)
 7. [Zoom](http://github.com/fungio/FungioGoogleMapBundle/blob/master/Resources/doc/usage/controls/zoom.md)
