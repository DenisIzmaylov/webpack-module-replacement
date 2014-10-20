Fork from standard Webpack Normal Module Replacement plugin to support a callback as a newResource.

Example:
```javascript
...
            plugins: [
                new webpack.NormalModuleReplacementPlugin(
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
