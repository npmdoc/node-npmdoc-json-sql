# api documentation for  [json-sql (v0.3.10)](https://github.com/2do2go/json-sql#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-json-sql.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-json-sql) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-json-sql.svg)](https://travis-ci.org/npmdoc/node-npmdoc-json-sql)
#### node.js json to sql queries mapper

[![NPM](https://nodei.co/npm/json-sql.png?downloads=true)](https://www.npmjs.com/package/json-sql)

[![apidoc](https://npmdoc.github.io/node-npmdoc-json-sql/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-json-sql_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-json-sql/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-json-sql/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-json-sql/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Artem Zhukov",
        "email": "artzhuchka@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/2do2go/json-sql/issues"
    },
    "dependencies": {
        "underscore": "1.8.2"
    },
    "description": "node.js json to sql queries mapper",
    "devDependencies": {
        "chai": "2.2.0",
        "gulp": "^3.8.11",
        "gulp-istanbul": "^0.10.0",
        "gulp-jshint": "^1.10.0",
        "gulp-mocha": "^2.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "2855ef05361531babb4a27c01d1ec47355b21fcb",
        "tarball": "https://registry.npmjs.org/json-sql/-/json-sql-0.3.10.tgz"
    },
    "gitHead": "7ecffc567086ca6080fb3d6cb60caed5d86043ca",
    "homepage": "https://github.com/2do2go/json-sql#readme",
    "keywords": [
        "json-sql",
        "json",
        "sql",
        "odm",
        "mapper",
        "db",
        "database"
    ],
    "license": "MIT",
    "main": "./lib/index",
    "maintainers": [
        {
            "name": "2do2go",
            "email": "dev.2do2go@gmail.com"
        }
    ],
    "name": "json-sql",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/2do2go/json-sql.git"
    },
    "scripts": {},
    "version": "0.3.10"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module json-sql](#apidoc.module.json-sql)
1.  [function <span class="apidocSignatureSpan">json-sql.</span>Builder (options)](#apidoc.element.json-sql.Builder)
1.  object <span class="apidocSignatureSpan">json-sql.</span>Builder.prototype

#### [module json-sql.Builder](#apidoc.module.json-sql.Builder)
1.  [function <span class="apidocSignatureSpan">json-sql.</span>Builder (options)](#apidoc.element.json-sql.Builder.Builder)

#### [module json-sql.Builder.prototype](#apidoc.module.json-sql.Builder.prototype)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_getPlaceholder ()](#apidoc.element.json-sql.Builder.prototype._getPlaceholder)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_pushValue (value)](#apidoc.element.json-sql.Builder.prototype._pushValue)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_reset ()](#apidoc.element.json-sql.Builder.prototype._reset)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_wrapPlaceholder (name)](#apidoc.element.json-sql.Builder.prototype._wrapPlaceholder)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>build (params)](#apidoc.element.json-sql.Builder.prototype.build)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>configure (options)](#apidoc.element.json-sql.Builder.prototype.configure)
1.  [function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>setDialect (name)](#apidoc.element.json-sql.Builder.prototype.setDialect)



# <a name="apidoc.module.json-sql"></a>[module json-sql](#apidoc.module.json-sql)

#### <a name="apidoc.element.json-sql.Builder"></a>[function <span class="apidocSignatureSpan">json-sql.</span>Builder (options)](#apidoc.element.json-sql.Builder)
- description and source-code
```javascript
Builder = function (options) {
	this.configure(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-sql.Builder"></a>[module json-sql.Builder](#apidoc.module.json-sql.Builder)

#### <a name="apidoc.element.json-sql.Builder.Builder"></a>[function <span class="apidocSignatureSpan">json-sql.</span>Builder (options)](#apidoc.element.json-sql.Builder.Builder)
- description and source-code
```javascript
Builder = function (options) {
	this.configure(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-sql.Builder.prototype"></a>[module json-sql.Builder.prototype](#apidoc.module.json-sql.Builder.prototype)

#### <a name="apidoc.element.json-sql.Builder.prototype._getPlaceholder"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_getPlaceholder ()](#apidoc.element.json-sql.Builder.prototype._getPlaceholder)
- description and source-code
```javascript
_getPlaceholder = function () {
	var placeholder = '';
	if (this.options.namedValues) placeholder += 'p';
	if (this.options.indexedValues) placeholder += this._placeholderId++;
	return placeholder;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-sql.Builder.prototype._pushValue"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_pushValue (value)](#apidoc.element.json-sql.Builder.prototype._pushValue)
- description and source-code
```javascript
_pushValue = function (value) {
	if (_.isUndefined(value) || _.isNull(value)) {
		return 'null';
	} else if (_.isNumber(value) || _.isBoolean(value)) {
		return String(value);
	} else if (_.isString(value) || _.isDate(value)) {
		if (this.options.separatedValues) {
			var placeholder = this._getPlaceholder();

			if (this.options.namedValues) {
				this._values[placeholder] = value;
			} else {
				this._values.push(value);
			}

			return this._wrapPlaceholder(placeholder);
		} else {
			if (_.isDate(value)) value = value.toISOString();

			return '\'' + value + '\'';
		}
	} else {
		throw new Error('Wrong value type "' + (typeof value) + '"');
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-sql.Builder.prototype._reset"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_reset ()](#apidoc.element.json-sql.Builder.prototype._reset)
- description and source-code
```javascript
_reset = function () {
	if (this.options.separatedValues) {
		this._placeholderId = 1;
		this._values = this.options.namedValues ? {} : [];
	} else {
		delete this._placeholderId;
		delete this._values;
	}

	this._query = '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-sql.Builder.prototype._wrapPlaceholder"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>_wrapPlaceholder (name)](#apidoc.element.json-sql.Builder.prototype._wrapPlaceholder)
- description and source-code
```javascript
_wrapPlaceholder = function (name) {
	return this.options.valuesPrefix + name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-sql.Builder.prototype.build"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>build (params)](#apidoc.element.json-sql.Builder.prototype.build)
- description and source-code
```javascript
build = function (params) {
	var builder = this;

	this._reset();

	this._query = this.dialect.buildTemplate('query', {queryBody: params}) + ';';

	if (this.options.separatedValues) {
		return {
			query: this._query,
			values: this._values,
			prefixValues: function() {
				var values = {};
				_(this.getValuesObject()).each(function(value, name) {
					values[builder._wrapPlaceholder(name)] = value;
				});
				return values;
			},
			getValuesArray: function() {
				return _.isArray(this.values) ? this.values : _(this.values).values();
			},
			getValuesObject: function() {
				return _.isArray(this.values) ? _(_.range(1, this.values.length + 1)).object(this.values) :
					this.values;
			}
		};
	} else {
		return {query: this._query};
	}
}
```
- example usage
```shell
...
'''

Then:

''' js
var jsonSql = require('json-sql')();

var sql = jsonSql.build({
	type: 'select',
	table: 'users',
	fields: ['name', 'age'],
	condition: {name: 'Max', id: 6}
});

sql.query
...
```

#### <a name="apidoc.element.json-sql.Builder.prototype.configure"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>configure (options)](#apidoc.element.json-sql.Builder.prototype.configure)
- description and source-code
```javascript
configure = function (options) {
	options = _.defaults({}, options, {
		separatedValues: true,
		namedValues: true,
		valuesPrefix: '$',
		dialect: 'base',
		wrappedIdentifiers: true,
		indexedValues: true
	});

	if (options.namedValues && !options.indexedValues) {
		throw new Error(
			'Option 'indexedValues': false is ' +
			'not allowed together with option 'namedValues': true'
		);
	}

	this.options = options;

	this.setDialect(this.options.dialect);

	this._reset();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-sql.Builder.prototype.setDialect"></a>[function <span class="apidocSignatureSpan">json-sql.Builder.prototype.</span>setDialect (name)](#apidoc.element.json-sql.Builder.prototype.setDialect)
- description and source-code
```javascript
setDialect = function (name) {
	if (!dialectsHash[name]) {
		throw new Error('Unknown dialect "' + name + '"');
	}

	this.dialect = new (dialectsHash[name])(this);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
