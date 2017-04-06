# api documentation for  [ember-cli-admin (v0.6.13)](http://ember-admin.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-ember-cli-admin.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ember-cli-admin) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ember-cli-admin.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ember-cli-admin)
#### Powerful admin dashboard for ember-cli projects, more in http://ember-admin.com

[![NPM](https://nodei.co/npm/ember-cli-admin.png?downloads=true)](https://www.npmjs.com/package/ember-cli-admin)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ember-cli-admin/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ember-cli-admin_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ember-cli-admin/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ember-cli-admin/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ember-cli-admin/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Alex Opak",
        "email": "opak.alexandr@gmail.com",
        "url": "https://github.com/OpakAlex"
    },
    "bugs": {
        "url": "https://github.com/ember-admin/ember-cli-admin/issues"
    },
    "contributors": [
        {
            "name": "Igor Kurinnoy",
            "email": "kurinnoyi@gmail.com",
            "url": "https://github.com/igorrKurr"
        },
        {
            "name": "Valeria Leshchenko",
            "email": "valeria.leshchenko@gmail.com",
            "url": "https://github.com/ValeriaLeshchenko"
        }
    ],
    "dependencies": {
        "broccoli-funnel": "^0.2.3",
        "chalk": "^1.1.1",
        "ember-cli-babel": "^5.0.0",
        "ember-cli-htmlbars": "0.7.9",
        "inflection": "^1.8.0"
    },
    "description": "Powerful admin dashboard for ember-cli projects, more in http://ember-admin.com",
    "devDependencies": {
        "active-model-adapter": "1.13.3",
        "broccoli-asset-rev": "^2.0.2",
        "broccoli-concat": "0.0.12",
        "broccoli-merge-trees": "^0.2.1",
        "broccoli-static-compiler": "^0.2.1",
        "ember-cli": "1.13.8",
        "ember-cli-app-version": "0.3.3",
        "ember-cli-bootstrap-datepicker": "0.5.3",
        "ember-cli-content-security-policy": "0.4.0",
        "ember-cli-dependency-checker": "^1.0.0",
        "ember-cli-inject-live-reload": "^1.3.0",
        "ember-cli-map": "0.4.2",
        "ember-cli-mirage": "0.1.8",
        "ember-cli-qunit": "0.3.15",
        "ember-cli-sass": "4.0.0-beta.5",
        "ember-cli-uglify": "1.0.1",
        "ember-data": "2.1.0",
        "ember-disable-prototype-extensions": "^1.0.0",
        "ember-disable-proxy-controllers": "^1.0.0",
        "ember-export-application-global": "^1.0.2",
        "ember-try": "0.0.7",
        "ember-watson": "^0.5.0"
    },
    "directories": {
        "doc": "doc",
        "test": "tests"
    },
    "dist": {
        "shasum": "c93e017489ca2a956d040b7bcbbe9df288c22f61",
        "tarball": "https://registry.npmjs.org/ember-cli-admin/-/ember-cli-admin-0.6.13.tgz"
    },
    "ember-addon": {
        "configPath": "tests/dummy/config",
        "demoURL": "http://rails.ember-admin.com/"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "81e7f3b924cf2c63e2a5624b82ff7b92307540ac",
    "homepage": "http://ember-admin.com",
    "keywords": [
        "ember-addon",
        "ember-cli",
        "admin",
        "ember",
        "ember-cli-admin",
        "ember-admin",
        "bootstrap-admin"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "valeria",
            "email": "valeria.leshchenko@gmail.com"
        },
        {
            "name": "opak",
            "email": "opak.alexandr@gmail.com"
        },
        {
            "name": "igorkur",
            "email": "kur91@mail.ru"
        }
    ],
    "name": "ember-cli-admin",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/ember-admin/ember-cli-admin.git"
    },
    "scripts": {
        "build": "ember build",
        "start": "ember server",
        "test": "ember try:testall"
    },
    "version": "0.6.13"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ember-cli-admin](#apidoc.module.ember-cli-admin)
1.  [function <span class="apidocSignatureSpan">ember-cli-admin.</span>included (app)](#apidoc.element.ember-cli-admin.included)
1.  [function <span class="apidocSignatureSpan">ember-cli-admin.</span>treeForPublic ()](#apidoc.element.ember-cli-admin.treeForPublic)
1.  string <span class="apidocSignatureSpan">ember-cli-admin.</span>name



# <a name="apidoc.module.ember-cli-admin"></a>[module ember-cli-admin](#apidoc.module.ember-cli-admin)

#### <a name="apidoc.element.ember-cli-admin.included"></a>[function <span class="apidocSignatureSpan">ember-cli-admin.</span>included (app)](#apidoc.element.ember-cli-admin.included)
- description and source-code
```javascript
included = function (app) {
  this.app = app;
  app.import(app.bowerDirectory + '/bootstrap-sass-official/assets/javascripts/bootstrap.js');
  app.import('vendor/fileicon.png', { destDir: 'assets/images' });
  app.import(app.bowerDirectory + '/typeahead.js/dist/bloodhound.min.js');
  app.import(app.bowerDirectory + '/typeahead.js/dist/typeahead.jquery.js');
  app.import(app.bowerDirectory + '/jquery-ui-sortable/jquery-ui-sortable.js');
  app.import(app.bowerDirectory + '/jquery-ui-touch-punch-improved/jquery.ui.touch-punch-improved.js');
  app.import('vendor/nested-sortable.js');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ember-cli-admin.treeForPublic"></a>[function <span class="apidocSignatureSpan">ember-cli-admin.</span>treeForPublic ()](#apidoc.element.ember-cli-admin.treeForPublic)
- description and source-code
```javascript
treeForPublic = function () {
  var bootstrapFonts = path.join(this.app.bowerDirectory, '/bootstrap-sass-official/assets/fonts/bootstrap');
  var bootstrapFontsTree = new Funnel(this.treeGenerator(bootstrapFonts), {
    srcDir: '/',
    destDir: '/fonts/bootstrap'
  });

  return bootstrapFontsTree;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
