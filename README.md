#!/usr/bin/env node

var libs = process.cwd() + '/libs/';
var config = require(libs + 'config');
var log = require(libs + 'log')(module);
var app = require(libs + 'app');

app.set('port', process.env.PORT || config.get('port') || 3000);

var server = app.listen(app.get('port'), function () {
  log.info('Express server listening on port ' + app.get('port'));
});# PostmanCollection
implementation of APIs
