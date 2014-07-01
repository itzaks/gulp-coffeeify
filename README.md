# gulp-coffeeify

Gulp task for browserify with coffee-script.

## USAGE

### Example

```javascript
var gulp = require('gulp');
var cofeeify = require('gulp-coffeeify');

// Basic usage
gulp.task('scripts', function() {
	gulp.src('src/coffee/**/*.coffee')
		.pipe(coffeeify())
		.pipe(gulp.dest('./build/js'))
});
```

## Options

### aliases

```javascript
var gulp = require('gulp');
var cofeeify = require('gulp-coffeeify');
gulp.task('scripts', function() {
  gulp.src('src/coffee/**/*.coffee')
    .pipe(coffeeify({
      aliases: [
        {
          cwd: 'src/coffee/app'
          base: 'app'
          file: ['**/*.coffee']
        }
      ]
    }))
    .pipe(gulp.dest('./build/js'))
});
```

You can use `src/coffee/app/views/View.coffee` as `app/views/View.coffee`

## License
Copyright (c) 2014 Yusuke Narita
Licensed under the MIT license.