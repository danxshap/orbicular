# CSS Circular Progress Bar

[![Build Status](https://travis-ci.org/cotag/orbicular.svg?branch=master)](https://travis-ci.org/cotag/orbicular)


Based on the technique used at http://fromanegg.com/post/41302147556/100-pure-css-radial-progress-bar

For cool auto-scaling UI's that require circular progression

![image](https://cloud.githubusercontent.com/assets/368013/2675921/6a099290-c127-11e3-9643-29a8b7ec6a9d.png)


## Installation

NOTE:: The [SCSS](http://sass-lang.com/) stylesheet uses [Compass](http://compass-style.org/install/) imports

1. Open bower.json
2. Add `"orbicular": "~2.0.0"` to your dependency list
3. Run `bower install`
4. In your application you can now add:
   * `<script src="bower_components/orbicular/orbicular/orbicular.js"></script>`
5. Copy / include the SCSS files into your project
   * Customise the styles using `_orbicular_config.scss`


## Usage

### Create your progress element

```html
<orbicular progression="downloaded" total="size">Text / HTML in the circle</orbicular>
```

Where `$scope.downloaded` (download progress) and `$scope.size` (total size of download) are the variables used in the example to track the progress of a download.


### Element size

The circles size is based on the width of the parent element.

This size is static and is set at the following times:

1. when the directive is linked
2. on mobile device rotation
3. when the browser window is resized
4. on the $broadcast of `'orb width'` to the elements scope

Broadcasting or emitting should be used to programmatically resize circles


## Upgrading from version 1.x.x

There is a single breaking change: (resolving a conflict with bootstrap UI)

* `progress="downloaded"` changes to `progression="downloaded"`


