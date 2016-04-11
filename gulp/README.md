## How to setup babel with gulp

Create `.babelrc` file with

```
{
    "presets": ["es2015"]
}
```

Install gulp-babel and presets

```
npm install gulp-babel babel-preset-es2015 --save-dev
```

Create file `gulpfile.js` with following code:

```js
var gulp = require('gulp');
var babel = require('gulp-babel');

gulp.task('babel', function() {
    return gulp.src('main.js')
      .pipe(babel())
      .pipe(gulp.dest('dist'));
});

gulp.task('watch', function() {
    gulp.watch('main.js', ['babel']);
});

gulp.task('default', ['watch']);
```

Run a gulp task

```
gulp
```

`main.js` with es6 will be transform to es5 in `dist/main.js`