# Mix Options

```js
mix.options({
    processCssUrls: true,
    uglify: {},
    purifyCss: false,
    //purifyCss: {},
    postCss: [require('autoprefixer')],
    clearConsole: false
});
```

A handful of Mix options and overrides are available, should you require them. Please take note of the options above, as well as their default values. Here's a quick overview:

* **processCssUrls:** Process/optimize relative stylesheet url()'s. By default, Webpack will automatically update these URLs, when relevant. If, however, your folder structure is already organized the way you want it, set this option to `false` to disable processing.
* **uglify:** Use this option to merge any [custom Uglify options](https://webpack.github.io/docs/list-of-plugins.html#uglifyjsplugin) that your project requires.
* **purifyCss:** Set this option to `true` if you want Mix to automatically read your HTML/Blade files and strip your CSS bundle of all unused selectors. You can also pass an object containing [purifycss-webpack options](https://github.com/webpack-contrib/purifycss-webpack#options).
* **postCss:** Merge any custom postcss plugins.
* **clearConsole:** Set this to false, if you don't want the terminal/console to clear after each build.
