*This repository is a mirror of the [component](http://component.io) module [yields/approximate-time](http://github.com/yields/approximate-time). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/yields-approximate-time`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# approximate-time

  approximate human readable time

## Installation

  Install with [component(1)](http://component.io):

    $ component install yields/approximate-time

## API

### approximate(date)

  Get approximate human readable time with `date`.

## Examples

```js
var time = require('approximate-time');

// now
assert('just now' == time(new Date));

// seconds
assert('a second' == time(add(1e3)));
assert('5 seconds' == time(add(1e3 * 5)));

// minutes
assert('a minute' == time(add(1e3 * 60)));
assert('5 minutes' == time(add(6e4 * 5)));

// hours
assert('an hour' == time(add(6e4 * 60)));
assert('5 hours' == time(add(3.6e+6 * 5)));

// days
assert('a day' == time(add(3.6e+6 * 24)));
assert('5 days' == time(add(8.64e+7 * 5)));

// weeks
assert('a week' == time(add(8.64e+7 * 7)));
assert('3 weeks' == time(add(6.048e+8 * 3)));

// months
assert('a month' == time(add(6.048e+8 * 4.4)));
assert('5 months' == time(add(2.63e+9 * 5)));

// years
assert('a year' == time(add(2.63e+9 * 12)));
assert('5 years' == time(add(3.156e+10 * 5)));

// decades
assert('a decade' == time(add(3.156e+10 * 10)));
assert('5 decades' == time(add(3.156e+11 * 5)));
assert('100 decades' == time(sub(3.156e+11 * 100)));
```

## License

  MIT
