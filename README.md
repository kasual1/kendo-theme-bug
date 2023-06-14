# KendoThemeBug

To reproduce the errors please complete the following steps.

```
clone the repository
```

```
npm install
```

```
npm run start
```

During the compilation process Angular throws many warnings originating in the ./src/styles.scss and fails with 2 errors. 

Namely:
```
./src/styles.scss - Error: Module Error (from ./node_modules/postcss-loader/dist/cjs.js):
C:\Projects\kendo-theme-bug\node_modules\@progress\kendo-theme-default\dist\all.scss:29953:8: Can't resolve 'null' in 'C:\Projects\kendo-theme-bug\src'

./src/styles.scss - Error: Module Error (from ./node_modules/postcss-loader/dist/cjs.js):
C:\Projects\kendo-theme-bug\node_modules\@progress\kendo-theme-default\dist\all.scss:45242:12: Can't resolve 'null' in 'C:\Projects\kendo-theme-bug\src'
```

To consistently reproduce the error with each build I disabled Angular caching in the angular.json ("cache": { "enabled": false })
