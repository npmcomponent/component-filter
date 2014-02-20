*This repository is a mirror of the [component](http://component.io) module [component/filter](http://github.com/component/filter). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-filter`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# filter

  dynamic dom node filtering via callback.

## Installation

    $ component install component/filter

## Example

 When list items contain the relevant text a `.hide` class is added
 for styling the filter.

```js
var filter = require('filter');
var ul = document.querySelector('ul');
var input = document.querySelector('input');

input.onkeyup = function(e){
  var str = input.value;
  filter(ul, function(li){
    return ~li.textContent.indexOf(str);
  });
};
```

## License

  MIT
