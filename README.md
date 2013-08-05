## Ember + Leaflet = Fun with maps! [![Build Status](https://secure.travis-ci.org/gabesmed/ember-leaflet.png?branch=master)](http://travis-ci.org/gabesmed/ember-leaflet)

EmberLeaflet aims to make working with Leaflet layers in your Ember app as **easy, declarative and composable** as Ember's View classes make working with DOM elements.

Wherever possible, the design is analogous to Ember's View, CollectionView and ContainerView architecture. EmberLeaflet provides functionality for maps, tile layers, markers, polylines and geometry, and popups. It provides hooks wherever possible for easy extensibility into more custom Leaflet behavior.

Full docs and live examples at [gabesmed.github.io/ember-leaflet](http://gabesmed.github.io/ember-leaflet).

## Usage

Creating a map is just one line of code!

``` javascript
App.AMapView = EmberLeaflet.MapView.extend({});
```

Create layers and bind content declaratively in idiomatic Ember.

``` javascript
App.AnotherMapView = EmberLeaflet.MapView.extend({
    childLayers: [
        App.TileLayer,
        EmberLeaflet.MarkerCollectionLayer.extend({
            contentBinding: 'controller'
        })]
});
```

Functionality is added to classes with mixins.

``` javascript
App.DraggableMarker = EmberLeaflet.MarkerLayer.extend(
    EmberLeaflet.DraggableMixin, {});
```

More examples at [gabesmed.github.io/ember-leaflet](http://gabesmed.github.io/ember-leaflet)

## Build It

1. `git clone https://github.com/gabesmed/ember-leaflet.git`
2. `bundle`
3. `bundle exec rake dist`
4. `cp dist/modules/ember-leaflet.js myapp/`

## Running unit tests

Run ```bundle exec rackup``` and open [http://localhost:9292](http://localhost:9292) in a browser.

## Thanks

* Thanks to the contributors to [emberjs/list-view](https://github.com/emberjs/list-view), from whom I cribbed this project skeleton.
* Thanks to everyone who makes Ember a joy to work with!
* Thanks to the makers of Leaflet, hooray for maps!