Schema Form Localizes String Add-on
===================================
 
**sf-simple-mde** add-on is used to upload files and store the file DTO's in the form model.

Installation
------------

```
$ bower install sf-simple-mde --save
```

Alternatively:

```
$ bower install https://github.com/obiba/sf-simple-mde.git#<release-number> --save
```


Make sure to include `sf-simple-mde.min.js` in your index file and load the module in your application:

```
var myModule = angular.module('myModule', [
 ...
 'sfObibaSimpleMde','hc.marked'
]);
```

Usage
-----

The schema:

```
"name": {
  "type": "object",
  "format": "simpleMde",
  "title": "Name",
  "description": "Name or alias",
  "maxLength": 10,
  "minLength": 2,
  "required": true
}
```

The Definition:

```
{
  "type":"simpleMde",
  "key":"name",
  "showLocales": true
}
```

To enable markdown support, the definition must have the properties ``` rows ``` bigger or equal to  ``` 2 ``` and ``` marked ``` set to ``` true ```.

Example Definition:

```
{
  "type":"simpleMde",
  "key":"name",
  "showLocales": true,
  "rows": 2,
  "marked": true
}
```

Events
------


| Name          | Type          | What |
| ------------- |:-------------:| -----|
| sfObibaSimpleMdeLocaleChanged| String        | changes the current locale|
