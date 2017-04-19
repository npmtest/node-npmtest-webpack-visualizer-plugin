# npmtest-webpack-visualizer-plugin

#### test coverage for  [webpack-visualizer-plugin (v0.1.11)](https://github.com/chrisbateman/webpack-visualizer#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-webpack-visualizer-plugin.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-webpack-visualizer-plugin) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-webpack-visualizer-plugin.svg)](https://travis-ci.org/npmtest/node-npmtest-webpack-visualizer-plugin)

#### Visualize and analyze your Webpack bundle to see which modules are taking up space and which might be duplicates.

[![NPM](https://nodei.co/npm/webpack-visualizer-plugin.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/webpack-visualizer-plugin)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-webpack-visualizer-plugin/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-webpack-visualizer-plugin/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/test-report.html](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-webpack-visualizer-plugin/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Chris Bateman",
        "url": "http://cbateman.com/"
    },
    "bugs": {
        "url": "https://github.com/chrisbateman/webpack-visualizer/issues"
    },
    "dependencies": {
        "d3": "^3.5.6",
        "mkdirp": "^0.5.1",
        "react": "^0.14.0",
        "react-dom": "^0.14.0"
    },
    "description": "Visualize and analyze your Webpack bundle to see which modules are taking up space and which might be duplicates.",
    "devDependencies": {
        "babel": "^5.8.23",
        "babel-core": "^5.8.25",
        "babel-loader": "^5.3.2",
        "eslint": "^1.6.0",
        "eslint-plugin-react": "^3.5.1",
        "merge": "^1.2.0",
        "webpack": "^1.12.2",
        "webpack-dev-server": "^1.12.0"
    },
    "directories": {},
    "dist": {
        "shasum": "b8770ad86b4f652612c68b1b782253faf9f8a34e",
        "tarball": "https://registry.npmjs.org/webpack-visualizer-plugin/-/webpack-visualizer-plugin-0.1.11.tgz"
    },
    "engines": {
        "npm": ">=2.13.0"
    },
    "files": [
        "lib",
        "README.md"
    ],
    "gitHead": "ea9ed0b8e8c83b45c398aa7605f9d8478f031f23",
    "homepage": "https://github.com/chrisbateman/webpack-visualizer#readme",
    "license": "MIT",
    "main": "lib/plugin.js",
    "maintainers": [
        {
            "name": "chrisbateman"
        }
    ],
    "name": "webpack-visualizer-plugin",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/chrisbateman/webpack-visualizer.git"
    },
    "scripts": {
        "build": "npm run buildsite && npm run buildplugin",
        "buildplugin": "webpack src/plugin/main.jsx lib/pluginmain.js --config webpack.prod.js",
        "buildsite": "webpack src/site/main.jsx dist-site/build.js --config webpack.prod.js && babel-node src/site/serverRender.js",
        "dev": "webpack-dev-server --config webpack.dev.js",
        "lint": "eslint src --ext .js,.jsx",
        "postbuildplugin": "babel src/plugin/plugin.js --out-file lib/plugin.js && cp src/shared/style.css lib",
        "postbuildsite": "cp src/shared/style.css test/stats-demo.json dist-site",
        "prebuildplugin": "rm -rf lib && mkdir lib",
        "prebuildsite": "rm -rf dist-site && mkdir dist-site",
        "preversion": "npm run lint && npm run build",
        "publishSite": "git checkout gh-pages && cp dist-site/* . && git add . && git commit -m 'release' && git push origin gh-pages && git checkout master"
    },
    "version": "0.1.11"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
