# React Leaflet Locator

# Inject script for dev notes

Injection is using the `build-scripts` command. It is using the inject script inside of `scripts/inject`. Currently testing with `map.html`. The purpose of this is to be injectable into any vanilla html project via script tag and data set html tag. Test the `map.html` inside the `dist` folder once it's done building.

# Working with CORS for sanity

You will need to add your domain to sanity's `CORS Origins` list otherwise you will recieve a cors error and the dealers will not return.

Go to `The Outdoor Group Dealer Locator` sanity project located here: https://manage.sanity.io/projects/kzfz2ho3. You will then navigate to `settings > api > CORS Origins` and add your domain there. That should prevent a CORS error from popping up. 

# Example usage

```html
<html>
  <h2>Stand Alone Dealer Page</h2>
  <body>
    <div data-locator-container></div> <!-- This must have the data attribute 'data-locator-container'. This is where the map will be injected. -->
  </body>
 <script type="text/javascript" src="https://map-inject.netlify.app/bundle.js"></script>
  <script>
    const MapInject = window.MapInject
    new MapInject()
  </script>
</html>
```
