<p align="center">
  <img src="https://img.ly/static/logos/PE.SDK_Logo.svg" />
</p>

**You can find our latest examples at https://github.com/imgly/pesdk-web-examples.**

# PhotoEditor SDK for HTML5 Ruby/Rails Gem Demonstration
Rails Gem for easily integrating [PhotoEditor SDK](https://img.ly/photo-sdk?utm_campaign=Projects&utm_source=Github&utm_medium=Side_Projects&utm_content=Ruby-Gem-Demo) for HTML5 in Ruby on Rails.

## Note 
The [PhotoEditor SDK](https://img.ly/photo-sdk?utm_campaign=Projects&utm_source=Github&utm_medium=Side_Projects&utm_content=Ruby-Gem-Demo) is a product of img.ly GmbH. 
Please [request a license](https://img.ly/pricing?utm_campaign=Projects&utm_source=Github&utm_medium=Side_Projects&utm_content=Ruby-Gem-Demo). Please see `LICENSE.md` for licensing details.


## PhotoEditor SDK for HTML5.
The [PhotoEditor SDK](https://img.ly/photo-sdk?utm_campaign=Projects&utm_source=Github&utm_medium=Side_Projects&utm_content=Ruby-Gem-Demo) for HTML5 is a **fully customizable** photo editor which you can integrate into your Rails app within minutes.

### Setup the Rails asset pipeline

1. Reference Gem in your bundlers Gemfile. Open your `Gemfile` and insert
```ruby
...
gem 'pesdk-html5-rails', :git => 'https://github.com/imgly/pesdk-ruby-gem-demo.git'
...
```
2. Register javascript with the Rails asset pipeline. Open `/assets/javascripts/application.js` and insert the following lines 

```javascript
...
//= require react.production.min
//= require react-dom.production.min
//= require react-dom-server.browser.production.min
//= require styled-components.min
//= require photoeditorsdk
...
```

3. Create a custom javascript file or modify your `application.js` to initialize the PhotoEditor UI on window load as follows 

```javascript
...

window.onload = function () {
   PhotoEditorSDK.PhotoEditorSDKUI.init({
       container: '#pesdk',
       license: '', // <- replace this with the content of your license file. The JSON-object needs to be in string format
       image: '', // <- Image url or Image path relative to assets folder
       assetBaseUrl: '/assets',
  })
}
...

```

4. Now, put a `<div/>` element in the view 
```html
...
<div id="pesdk"  style="width: 1024px; height: 768px;">
...
```

## License
Please see [LICENSE](https://github.com/imgly/pesdk-ruby-gem-demo/blob/main/LICENSE.md) for licensing details.

## Authors and Contributors
Made 2013-2020 by img.ly

## Support or Contact
Use our [service desk](https://support.img.ly) for bug reports or support requests. To request a commercial license, please use the [license request form](https://img.ly/pricing?utm_campaign=Projects&utm_source=Github&utm_medium=Side_Projects&utm_content=Ruby-Gem-Demo) on our website.

