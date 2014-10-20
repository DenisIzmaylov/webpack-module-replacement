Fork from standard Webpack Normal Module Replacement plugin to support a callback as a newResource.

##Installation
`npm install DenisIzmaylov/webpack-module-replacement`

##Usage
```javascript
var ModuleReplacementPlugin = require('webpack-module-replacement');

...
            plugins: [
                new ModuleReplacementPlugin(
                    /\.css$/,
                    function (request) {
                        request.context = path.join(
                            buildSettings.destPath,
                            path.relative(buildSettings.sourcePath, request.context)
                        );
                    }
                )
            ]
...
```

##TODO
- Merge code from ContextReplacementPlugin
