# api documentation for  [chokidar (v1.6.1)](https://github.com/paulmillr/chokidar)  [![npm package](https://img.shields.io/npm/v/npmdoc-chokidar.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-chokidar) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-chokidar.svg)](https://travis-ci.org/npmdoc/node-npmdoc-chokidar)
#### A neat wrapper around node.js fs.watch / fs.watchFile / fsevents.

[![NPM](https://nodei.co/npm/chokidar.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/chokidar)

[![apidoc](https://npmdoc.github.io/node-npmdoc-chokidar/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-chokidar/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-chokidar/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-chokidar/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Miller",
        "url": "http://paulmillr.com"
    },
    "bugs": {
        "url": "http://github.com/paulmillr/chokidar/issues"
    },
    "dependencies": {
        "anymatch": "^1.3.0",
        "async-each": "^1.0.0",
        "fsevents": "^1.0.0",
        "glob-parent": "^2.0.0",
        "inherits": "^2.0.1",
        "is-binary-path": "^1.0.0",
        "is-glob": "^2.0.0",
        "path-is-absolute": "^1.0.0",
        "readdirp": "^2.0.0"
    },
    "description": "A neat wrapper around node.js fs.watch / fs.watchFile / fsevents.",
    "devDependencies": {
        "chai": "^3.2.0",
        "coveralls": "^2.11.2",
        "graceful-fs": "4.1.4",
        "istanbul": "^0.3.20",
        "mocha": "^2.0.0",
        "rimraf": "^2.4.3",
        "sinon": "^1.10.3",
        "sinon-chai": "^2.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "2f4447ab5e96e50fb3d789fd90d4c72e0e4c70c2",
        "tarball": "https://registry.npmjs.org/chokidar/-/chokidar-1.6.1.tgz"
    },
    "files": [
        "index.js",
        "lib/"
    ],
    "gitHead": "c08145c5368fac6441773e621da9db215cc0d3b2",
    "homepage": "https://github.com/paulmillr/chokidar",
    "keywords": [
        "fs",
        "watch",
        "watchFile",
        "watcher",
        "watching",
        "file",
        "fsevents"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "paulmillr"
        },
        {
            "name": "es128"
        }
    ],
    "name": "chokidar",
    "optionalDependencies": {
        "fsevents": "^1.0.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/paulmillr/chokidar.git"
    },
    "scripts": {
        "ci-test": "istanbul cover _mocha && cat ./coverage/lcov.info | coveralls",
        "test": "istanbul test node_modules/mocha/bin/_mocha"
    },
    "version": "1.6.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module chokidar](#apidoc.module.chokidar)
1.  [function <span class="apidocSignatureSpan">chokidar.</span>FSWatcher (_opts)](#apidoc.element.chokidar.FSWatcher)
1.  [function <span class="apidocSignatureSpan">chokidar.</span>fsevents_handler ()](#apidoc.element.chokidar.fsevents_handler)
1.  [function <span class="apidocSignatureSpan">chokidar.</span>watch (paths, options)](#apidoc.element.chokidar.watch)
1.  object <span class="apidocSignatureSpan">chokidar.</span>FSWatcher.prototype
1.  object <span class="apidocSignatureSpan">chokidar.</span>fsevents_handler.prototype

#### [module chokidar.FSWatcher](#apidoc.module.chokidar.FSWatcher)
1.  [function <span class="apidocSignatureSpan">chokidar.</span>FSWatcher (_opts)](#apidoc.element.chokidar.FSWatcher.FSWatcher)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.</span>super_ ()](#apidoc.element.chokidar.FSWatcher.super_)

#### [module chokidar.FSWatcher.prototype](#apidoc.module.chokidar.FSWatcher.prototype)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_addToNodeFs (path, initialAdd, priorWh, depth, target, callback)](#apidoc.element.chokidar.FSWatcher.prototype._addToNodeFs)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_awaitWriteFinish (path, threshold, event, awfEmit)](#apidoc.element.chokidar.FSWatcher.prototype._awaitWriteFinish)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_closePath (path)](#apidoc.element.chokidar.FSWatcher.prototype._closePath)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_emit (event, path, val1, val2, val3)](#apidoc.element.chokidar.FSWatcher.prototype._emit)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_getWatchHelpers (path, depth)](#apidoc.element.chokidar.FSWatcher.prototype._getWatchHelpers)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_getWatchedDir (directory)](#apidoc.element.chokidar.FSWatcher.prototype._getWatchedDir)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleDir (dir, stats, initialAdd, depth, target, wh, callback)](#apidoc.element.chokidar.FSWatcher.prototype._handleDir)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleError (error)](#apidoc.element.chokidar.FSWatcher.prototype._handleError)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleFile (file, stats, initialAdd, callback)](#apidoc.element.chokidar.FSWatcher.prototype._handleFile)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleSymlink (entry, directory, path, item)](#apidoc.element.chokidar.FSWatcher.prototype._handleSymlink)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_hasReadPermissions (stats)](#apidoc.element.chokidar.FSWatcher.prototype._hasReadPermissions)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_isIgnored (path, stats)](#apidoc.element.chokidar.FSWatcher.prototype._isIgnored)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_remove (directory, item)](#apidoc.element.chokidar.FSWatcher.prototype._remove)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_throttle (action, path, timeout)](#apidoc.element.chokidar.FSWatcher.prototype._throttle)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_watchWithNodeFs (path, listener)](#apidoc.element.chokidar.FSWatcher.prototype._watchWithNodeFs)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>add (paths, _origAdd, _internal)](#apidoc.element.chokidar.FSWatcher.prototype.add)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>close ()](#apidoc.element.chokidar.FSWatcher.prototype.close)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>getWatched ()](#apidoc.element.chokidar.FSWatcher.prototype.getWatched)
1.  [function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>unwatch (paths)](#apidoc.element.chokidar.FSWatcher.prototype.unwatch)

#### [module chokidar.fsevents_handler](#apidoc.module.chokidar.fsevents_handler)
1.  [function <span class="apidocSignatureSpan">chokidar.</span>fsevents_handler ()](#apidoc.element.chokidar.fsevents_handler.fsevents_handler)
1.  [function <span class="apidocSignatureSpan">chokidar.fsevents_handler.</span>canUse ()](#apidoc.element.chokidar.fsevents_handler.canUse)

#### [module chokidar.fsevents_handler.prototype](#apidoc.module.chokidar.fsevents_handler.prototype)
1.  [function <span class="apidocSignatureSpan">chokidar.fsevents_handler.prototype.</span>_addToFsEvents (path, transform, forceAdd, priorDepth)](#apidoc.element.chokidar.fsevents_handler.prototype._addToFsEvents)
1.  [function <span class="apidocSignatureSpan">chokidar.fsevents_handler.prototype.</span>_handleFsEventsSymlink (linkPath, fullPath, transform, curDepth)](#apidoc.element.chokidar.fsevents_handler.prototype._handleFsEventsSymlink)
1.  [function <span class="apidocSignatureSpan">chokidar.fsevents_handler.prototype.</span>_watchWithFsEvents (watchPath, realPath, transform, globFilter)](#apidoc.element.chokidar.fsevents_handler.prototype._watchWithFsEvents)



# <a name="apidoc.module.chokidar"></a>[module chokidar](#apidoc.module.chokidar)

#### <a name="apidoc.element.chokidar.FSWatcher"></a>[function <span class="apidocSignatureSpan">chokidar.</span>FSWatcher (_opts)](#apidoc.element.chokidar.FSWatcher)
- description and source-code
```javascript
function FSWatcher(_opts) {
  EventEmitter.call(this);
  var opts = {};
  // in case _opts that is passed in is a frozen object
  if (_opts) for (var opt in _opts) opts[opt] = _opts[opt];
  this._watched = Object.create(null);
  this._closers = Object.create(null);
  this._ignoredPaths = Object.create(null);
  Object.defineProperty(this, '_globIgnored', {
    get: function() { return Object.keys(this._ignoredPaths); }
  });
  this.closed = false;
  this._throttled = Object.create(null);
  this._symlinkPaths = Object.create(null);

  function undef(key) {
    return opts[key] === undefined;
  }

  // Set up default options.
  if (undef('persistent')) opts.persistent = true;
  if (undef('ignoreInitial')) opts.ignoreInitial = false;
  if (undef('ignorePermissionErrors')) opts.ignorePermissionErrors = false;
  if (undef('interval')) opts.interval = 100;
  if (undef('binaryInterval')) opts.binaryInterval = 300;
  this.enableBinaryInterval = opts.binaryInterval !== opts.interval;

  // Enable fsevents on OS X when polling isn't explicitly enabled.
  if (undef('useFsEvents')) opts.useFsEvents = !opts.usePolling;

  // If we can't use fsevents, ensure the options reflect it's disabled.
  if (!FsEventsHandler.canUse()) opts.useFsEvents = false;

  // Use polling on Mac if not using fsevents.
  // Other platforms use non-polling fs.watch.
  if (undef('usePolling') && !opts.useFsEvents) {
    opts.usePolling = process.platform === 'darwin';
  }

  // Global override (useful for end-developers that need to force polling for all
  // instances of chokidar, regardless of usage/dependency depth)
  var envPoll = process.env.CHOKIDAR_USEPOLLING;
  if (envPoll !== undefined) {
    var envLower = envPoll.toLowerCase();

    if (envLower === 'false' || envLower === '0') {
      opts.usePolling = false;
    } else if (envLower === 'true' || envLower === '1') {
      opts.usePolling = true;
    } else {
      opts.usePolling = !!envLower
    }
  }

  // Editor atomic write normalization enabled by default with fs.watch
  if (undef('atomic')) opts.atomic = !opts.usePolling && !opts.useFsEvents;
  if (opts.atomic) this._pendingUnlinks = Object.create(null);

  if (undef('followSymlinks')) opts.followSymlinks = true;

  if (undef('awaitWriteFinish')) opts.awaitWriteFinish = false;
  if (opts.awaitWriteFinish === true) opts.awaitWriteFinish = {};
  var awf = opts.awaitWriteFinish;
  if (awf) {
    if (!awf.stabilityThreshold) awf.stabilityThreshold = 2000;
    if (!awf.pollInterval) awf.pollInterval = 100;

    this._pendingWrites = Object.create(null);
  }
  if (opts.ignored) opts.ignored = arrify(opts.ignored);

  this._isntIgnored = function(path, stat) {
    return !this._isIgnored(path, stat);
  }.bind(this);

  var readyCalls = 0;
  this._emitReady = function() {
    if (++readyCalls >= this._readyCount) {
      this._emitReady = Function.prototype;
      this._readyEmitted = true;
      // use process.nextTick to allow time for listener to be bound
      process.nextTick(this.emit.bind(this, 'ready'));
    }
  }.bind(this);

  this.options = opts;

  // You’re frozen when your heart’s not open.
  Object.freeze(opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.fsevents_handler"></a>[function <span class="apidocSignatureSpan">chokidar.</span>fsevents_handler ()](#apidoc.element.chokidar.fsevents_handler)
- description and source-code
```javascript
function FsEventsHandler() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.watch"></a>[function <span class="apidocSignatureSpan">chokidar.</span>watch (paths, options)](#apidoc.element.chokidar.watch)
- description and source-code
```javascript
watch = function (paths, options) {
  return new FSWatcher(options).add(paths);
}
```
- example usage
```shell
...

Then 'require' and use it in your code:

'''javascript
var chokidar = require('chokidar');

// One-liner for current directory, ignores .dotfiles
chokidar.watch('.', {ignored: /[\/\\]\./}).on('all', (event, path) => {
  console.log(event, path);
});
'''

'''javascript
// Example of a more typical implementation structure:
...
```



# <a name="apidoc.module.chokidar.FSWatcher"></a>[module chokidar.FSWatcher](#apidoc.module.chokidar.FSWatcher)

#### <a name="apidoc.element.chokidar.FSWatcher.FSWatcher"></a>[function <span class="apidocSignatureSpan">chokidar.</span>FSWatcher (_opts)](#apidoc.element.chokidar.FSWatcher.FSWatcher)
- description and source-code
```javascript
function FSWatcher(_opts) {
  EventEmitter.call(this);
  var opts = {};
  // in case _opts that is passed in is a frozen object
  if (_opts) for (var opt in _opts) opts[opt] = _opts[opt];
  this._watched = Object.create(null);
  this._closers = Object.create(null);
  this._ignoredPaths = Object.create(null);
  Object.defineProperty(this, '_globIgnored', {
    get: function() { return Object.keys(this._ignoredPaths); }
  });
  this.closed = false;
  this._throttled = Object.create(null);
  this._symlinkPaths = Object.create(null);

  function undef(key) {
    return opts[key] === undefined;
  }

  // Set up default options.
  if (undef('persistent')) opts.persistent = true;
  if (undef('ignoreInitial')) opts.ignoreInitial = false;
  if (undef('ignorePermissionErrors')) opts.ignorePermissionErrors = false;
  if (undef('interval')) opts.interval = 100;
  if (undef('binaryInterval')) opts.binaryInterval = 300;
  this.enableBinaryInterval = opts.binaryInterval !== opts.interval;

  // Enable fsevents on OS X when polling isn't explicitly enabled.
  if (undef('useFsEvents')) opts.useFsEvents = !opts.usePolling;

  // If we can't use fsevents, ensure the options reflect it's disabled.
  if (!FsEventsHandler.canUse()) opts.useFsEvents = false;

  // Use polling on Mac if not using fsevents.
  // Other platforms use non-polling fs.watch.
  if (undef('usePolling') && !opts.useFsEvents) {
    opts.usePolling = process.platform === 'darwin';
  }

  // Global override (useful for end-developers that need to force polling for all
  // instances of chokidar, regardless of usage/dependency depth)
  var envPoll = process.env.CHOKIDAR_USEPOLLING;
  if (envPoll !== undefined) {
    var envLower = envPoll.toLowerCase();

    if (envLower === 'false' || envLower === '0') {
      opts.usePolling = false;
    } else if (envLower === 'true' || envLower === '1') {
      opts.usePolling = true;
    } else {
      opts.usePolling = !!envLower
    }
  }

  // Editor atomic write normalization enabled by default with fs.watch
  if (undef('atomic')) opts.atomic = !opts.usePolling && !opts.useFsEvents;
  if (opts.atomic) this._pendingUnlinks = Object.create(null);

  if (undef('followSymlinks')) opts.followSymlinks = true;

  if (undef('awaitWriteFinish')) opts.awaitWriteFinish = false;
  if (opts.awaitWriteFinish === true) opts.awaitWriteFinish = {};
  var awf = opts.awaitWriteFinish;
  if (awf) {
    if (!awf.stabilityThreshold) awf.stabilityThreshold = 2000;
    if (!awf.pollInterval) awf.pollInterval = 100;

    this._pendingWrites = Object.create(null);
  }
  if (opts.ignored) opts.ignored = arrify(opts.ignored);

  this._isntIgnored = function(path, stat) {
    return !this._isIgnored(path, stat);
  }.bind(this);

  var readyCalls = 0;
  this._emitReady = function() {
    if (++readyCalls >= this._readyCount) {
      this._emitReady = Function.prototype;
      this._readyEmitted = true;
      // use process.nextTick to allow time for listener to be bound
      process.nextTick(this.emit.bind(this, 'ready'));
    }
  }.bind(this);

  this.options = opts;

  // You’re frozen when your heart’s not open.
  Object.freeze(opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.FSWatcher.super_"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.</span>super_ ()](#apidoc.element.chokidar.FSWatcher.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.chokidar.FSWatcher.prototype"></a>[module chokidar.FSWatcher.prototype](#apidoc.module.chokidar.FSWatcher.prototype)

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._addToNodeFs"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_addToNodeFs (path, initialAdd, priorWh, depth, target, callback)](#apidoc.element.chokidar.FSWatcher.prototype._addToNodeFs)
- description and source-code
```javascript
_addToNodeFs = function (path, initialAdd, priorWh, depth, target, callback) {
  if (!callback) callback = Function.prototype;
  var ready = this._emitReady;
  if (this._isIgnored(path) || this.closed) {
    ready();
    return callback(null, false);
  }

  var wh = this._getWatchHelpers(path, depth);
  if (!wh.hasGlob && priorWh) {
    wh.hasGlob = priorWh.hasGlob;
    wh.globFilter = priorWh.globFilter;
    wh.filterPath = priorWh.filterPath;
    wh.filterDir = priorWh.filterDir;
  }

  // evaluate what is at the path we're being asked to watch
  fs[wh.statMethod](wh.watchPath, function(error, stats) {
    if (this._handleError(error)) return callback(null, path);
    if (this._isIgnored(wh.watchPath, stats)) {
      ready();
      return callback(null, false);
    }

    var initDir = function(dir, target) {
      return this._handleDir(dir, stats, initialAdd, depth, target, wh, ready);
    }.bind(this);

    var closer;
    if (stats.isDirectory()) {
      closer = initDir(wh.watchPath, target);
    } else if (stats.isSymbolicLink()) {
      var parent = sysPath.dirname(wh.watchPath);
      this._getWatchedDir(parent).add(wh.watchPath);
      this._emit('add', wh.watchPath, stats);
      closer = initDir(parent, path);

      // preserve this symlink's target path
      fs.realpath(path, function(error, targetPath) {
        this._symlinkPaths[sysPath.resolve(path)] = targetPath;
        ready();
      }.bind(this));
    } else {
      closer = this._handleFile(wh.watchPath, stats, initialAdd, ready);
    }

    if (closer) this._closers[path] = closer;
    callback(null, false);
  }.bind(this));
}
```
- example usage
```shell
...
  if (!this._readyCount) this._readyCount = paths.length;
  if (this.options.persistent) this._readyCount *= 2;
  paths.forEach(this._addToFsEvents, this);
} else {
  if (!this._readyCount) this._readyCount = 0;
  this._readyCount += paths.length;
  asyncEach(paths, function(path, next) {
    this._addToNodeFs(path, !_internal, 0, 0, _origAdd, function(err, res) {
      if (res) this._emitReady();
      next(err, res);
    }.bind(this));
  }.bind(this), function(error, results) {
    results.forEach(function(item) {
      if (!item) return;
      this.add(sysPath.dirname(item), sysPath.basename(_origAdd || item));
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._awaitWriteFinish"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_awaitWriteFinish (path, threshold, event, awfEmit)](#apidoc.element.chokidar.FSWatcher.prototype._awaitWriteFinish)
- description and source-code
```javascript
_awaitWriteFinish = function (path, threshold, event, awfEmit) {
  var timeoutHandler;

  var fullPath = path;
  if (this.options.cwd && !isAbsolute(path)) {
    fullPath = sysPath.join(this.options.cwd, path);
  }

  var now = new Date();

  var awaitWriteFinish = (function (prevStat) {
    fs.stat(fullPath, function(err, curStat) {
      if (err) {
        if (err.code !== 'ENOENT') awfEmit(err);
        return;
      }

      var now = new Date();

      if (prevStat && curStat.size != prevStat.size) {
        this._pendingWrites[path].lastChange = now;
      }

      if (now - this._pendingWrites[path].lastChange >= threshold) {
        delete this._pendingWrites[path];
        awfEmit(null, curStat);
      } else {
        timeoutHandler = setTimeout(
          awaitWriteFinish.bind(this, curStat),
          this.options.awaitWriteFinish.pollInterval
        );
      }
    }.bind(this));
  }.bind(this));

  if (!(path in this._pendingWrites)) {
    this._pendingWrites[path] = {
      lastChange: now,
      cancelWait: function() {
        delete this._pendingWrites[path];
        clearTimeout(timeoutHandler);
        return event;
      }.bind(this)
    };
    timeoutHandler = setTimeout(
      awaitWriteFinish.bind(this),
      this.options.awaitWriteFinish.pollInterval
    );
  }
}
```
- example usage
```shell
...
      } else {
        args.push(stats);
      }
      emitEvent();
    }
  };

  this._awaitWriteFinish(path, awf.stabilityThreshold, event, awfEmit);
  return this;
}

if (event === 'change') {
  if (!this._throttle('change', path, 50)) return this;
}
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._closePath"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_closePath (path)](#apidoc.element.chokidar.FSWatcher.prototype._closePath)
- description and source-code
```javascript
_closePath = function (path) {
  if (!this._closers[path]) return;
  this._closers[path]();
  delete this._closers[path];
  this._getWatchedDir(sysPath.dirname(path)).remove(sysPath.basename(path));
}
```
- example usage
```shell
...
delete this._watched[path];
delete this._watched[fullPath];
var eventName = isDirectory ? 'unlinkDir' : 'unlink';
if (wasTracked && !this._isIgnored(path)) this._emit(eventName, path);

// Avoid conflicts if we later create another file with the same name
if (!this.options.useFsEvents) {
  this._closePath(path);
}
};

FSWatcher.prototype._closePath = function(path) {
if (!this._closers[path]) return;
this._closers[path]();
delete this._closers[path];
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._emit"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_emit (event, path, val1, val2, val3)](#apidoc.element.chokidar.FSWatcher.prototype._emit)
- description and source-code
```javascript
_emit = function (event, path, val1, val2, val3) {
  if (this.options.cwd) path = sysPath.relative(this.options.cwd, path);
  var args = [event, path];
  if (val3 !== undefined) args.push(val1, val2, val3);
  else if (val2 !== undefined) args.push(val1, val2);
  else if (val1 !== undefined) args.push(val1);

  var awf = this.options.awaitWriteFinish;
  if (awf && this._pendingWrites[path]) {
    this._pendingWrites[path].lastChange = new Date();
    return this;
  }

  if (this.options.atomic) {
    if (event === 'unlink') {
      this._pendingUnlinks[path] = args;
      setTimeout(function() {
        Object.keys(this._pendingUnlinks).forEach(function(path) {
          this.emit.apply(this, this._pendingUnlinks[path]);
          this.emit.apply(this, ['all'].concat(this._pendingUnlinks[path]));
          delete this._pendingUnlinks[path];
        }.bind(this));
      }.bind(this), typeof this.options.atomic === "number"
        ? this.options.atomic
        : 100);
      return this;
    } else if (event === 'add' && this._pendingUnlinks[path]) {
      event = args[0] = 'change';
      delete this._pendingUnlinks[path];
    }
  }

  var emitEvent = function() {
    this.emit.apply(this, args);
    if (event !== 'error') this.emit.apply(this, ['all'].concat(args));
  }.bind(this);

  if (awf && (event === 'add' || event === 'change') && this._readyEmitted) {
    var awfEmit = function(err, stats) {
      if (err) {
        event = args[0] = 'error';
        args[1] = err;
        emitEvent();
      } else if (stats) {
        // if stats doesn't exist the file must have been deleted
        if (args.length > 2) {
          args[2] = stats;
        } else {
          args.push(stats);
        }
        emitEvent();
      }
    };

    this._awaitWriteFinish(path, awf.stabilityThreshold, event, awfEmit);
    return this;
  }

  if (event === 'change') {
    if (!this._throttle('change', path, 50)) return this;
  }

  if (
    this.options.alwaysStat && val1 === undefined &&
    (event === 'add' || event === 'addDir' || event === 'change')
  ) {
    var fullPath = this.options.cwd ? sysPath.join(this.options.cwd, path) : path;
    fs.stat(fullPath, function(error, stats) {
      // Suppress event when fs.stat fails, to avoid sending undefined 'stat'
      if (error || !stats) return;

      args.push(stats);
      emitEvent();
    });
  } else {
    emitEvent();
  }

  return this;
}
```
- example usage
```shell
...
  }

  // The Entry will either be a directory that just got removed
  // or a bogus entry to a file, in either case we have to remove it
  delete this._watched[path];
  delete this._watched[fullPath];
  var eventName = isDirectory ? 'unlinkDir' : 'unlink';
  if (wasTracked && !this._isIgnored(path)) this._emit(eventName, path);

  // Avoid conflicts if we later create another file with the same name
  if (!this.options.useFsEvents) {
    this._closePath(path);
  }
};
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._getWatchHelpers"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_getWatchHelpers (path, depth)](#apidoc.element.chokidar.FSWatcher.prototype._getWatchHelpers)
- description and source-code
```javascript
_getWatchHelpers = function (path, depth) {
  path = path.replace(replacerRe, '');
  var watchPath = depth || !isGlob(path) ? path : globParent(path);
  var fullWatchPath = sysPath.resolve(watchPath);
  var hasGlob = watchPath !== path;
  var globFilter = hasGlob ? anymatch(path) : false;
  var follow = this.options.followSymlinks;
  var globSymlink = hasGlob && follow ? null : false;

  var checkGlobSymlink = function(entry) {
    // only need to resolve once
    // first entry should always have entry.parentDir === ''
    if (globSymlink == null) {
      globSymlink = entry.fullParentDir === fullWatchPath ? false : {
        realPath: entry.fullParentDir,
        linkPath: fullWatchPath
      };
    }

    if (globSymlink) {
      return entry.fullPath.replace(globSymlink.realPath, globSymlink.linkPath);
    }

    return entry.fullPath;
  };

  var entryPath = function(entry) {
    return sysPath.join(watchPath,
      sysPath.relative(watchPath, checkGlobSymlink(entry))
    );
  };

  var filterPath = function(entry) {
    if (entry.stat && entry.stat.isSymbolicLink()) return filterDir(entry);
    var resolvedPath = entryPath(entry);
    return (!hasGlob || globFilter(resolvedPath)) &&
      this._isntIgnored(resolvedPath, entry.stat) &&
      (this.options.ignorePermissionErrors ||
        this._hasReadPermissions(entry.stat));
  }.bind(this);

  var getDirParts = function(path) {
    if (!hasGlob) return false;
    var parts = sysPath.relative(watchPath, path).split(/[\/\\]/);
    return parts;
  };

  var dirParts = getDirParts(path);
  if (dirParts && dirParts.length > 1) dirParts.pop();
  var unmatchedGlob;

  var filterDir = function(entry) {
    if (hasGlob) {
      var entryParts = getDirParts(checkGlobSymlink(entry));
      var globstar = false;
      unmatchedGlob = !dirParts.every(function(part, i) {
        if (part === '**') globstar = true;
        return globstar || !entryParts[i] || anymatch(part, entryParts[i]);
      });
    }
    return !unmatchedGlob && this._isntIgnored(entryPath(entry), entry.stat);
  }.bind(this);

  return {
    followSymlinks: follow,
    statMethod: follow ? 'stat' : 'lstat',
    path: path,
    watchPath: watchPath,
    entryPath: entryPath,
    hasGlob: hasGlob,
    globFilter: globFilter,
    filterPath: filterPath,
    filterDir: filterDir
  };
}
```
- example usage
```shell
...
  dirObj.add(base);

  if (!this.options.ignoreInitial || forceAdd === true) {
    this._emit(isDir ? 'addDir' : 'add', pp, stats);
  }
}.bind(this);

var wh = this._getWatchHelpers(path);

// evaluate what is at the path we're being asked to watch
fs[wh.statMethod](wh.watchPath, function(error, stats) {
  if (this._handleError(error) || this._isIgnored(wh.watchPath, stats)) {
    this._emitReady();
    return this._emitReady();
  }
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._getWatchedDir"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_getWatchedDir (directory)](#apidoc.element.chokidar.FSWatcher.prototype._getWatchedDir)
- description and source-code
```javascript
_getWatchedDir = function (directory) {
  var dir = sysPath.resolve(directory);
  var watcherRemove = this._remove.bind(this);
  if (!(dir in this._watched)) this._watched[dir] = {
    _items: Object.create(null),
    add: function(item) {
      if (item !== '.') this._items[item] = true;
    },
    remove: function(item) {
      delete this._items[item];
      if (!this.children().length) {
        fs.readdir(dir, function(err) {
          if (err) watcherRemove(sysPath.dirname(dir), sysPath.basename(dir));
        });
      }
    },
    has: function(item) {return item in this._items;},
    children: function() {return Object.keys(this._items);}
  };
  return this._watched[dir];
}
```
- example usage
```shell
...
var watchedDirs = Object.keys(this._watched);
if (!isDirectory && !this.options.useFsEvents && watchedDirs.length === 1) {
  this.add(directory, item, true);
}

// This will create a new entry in the watched object in either case
// so we got to do the directory check beforehand
var nestedDirectoryChildren = this._getWatchedDir(path).children();

// Recursively remove children directories / files.
nestedDirectoryChildren.forEach(function(nestedItem) {
  this._remove(path, nestedItem);
}, this);

// Check if item was on the watched list and remove it
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._handleDir"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleDir (dir, stats, initialAdd, depth, target, wh, callback)](#apidoc.element.chokidar.FSWatcher.prototype._handleDir)
- description and source-code
```javascript
_handleDir = function (dir, stats, initialAdd, depth, target, wh, callback) {
  var parentDir = this._getWatchedDir(sysPath.dirname(dir));
  var tracked = parentDir.has(sysPath.basename(dir));
  if (!(initialAdd && this.options.ignoreInitial) && !target && !tracked) {
    if (!wh.hasGlob || wh.globFilter(dir)) this._emit('addDir', dir, stats);
  }

  // ensure dir is tracked (harmless if redundant)
  parentDir.add(sysPath.basename(dir));
  this._getWatchedDir(dir);

  var read = function(directory, initialAdd, done) {
    // Normalize the directory name on Windows
    directory = sysPath.join(directory, '');

    if (!wh.hasGlob) {
      var throttler = this._throttle('readdir', directory, 1000);
      if (!throttler) return;
    }

    var previous = this._getWatchedDir(wh.path);
    var current = [];

    readdirp({
      root: directory,
      entryType: 'all',
      fileFilter: wh.filterPath,
      directoryFilter: wh.filterDir,
      depth: 0,
      lstat: true
    }).on('data', function(entry) {
      var item = entry.path;
      var path = sysPath.join(directory, item);
      current.push(item);

      if (entry.stat.isSymbolicLink() &&
        this._handleSymlink(entry, directory, path, item)) return;

      // Files that present in current directory snapshot
      // but absent in previous are added to watch list and
      // emit 'add' event.
      if (item === target || !target && !previous.has(item)) {
        this._readyCount++;

        // ensure relativeness of path is preserved in case of watcher reuse
        path = sysPath.join(dir, sysPath.relative(dir, path));

        this._addToNodeFs(path, initialAdd, wh, depth + 1);
      }
    }.bind(this)).on('end', function() {
      if (throttler) throttler.clear();
      if (done) done();

      // Files that absent in current directory snapshot
      // but present in previous emit 'remove' event
      // and are removed from @watched[directory].
      previous.children().filter(function(item) {
        return item !== directory &&
          current.indexOf(item) === -1 &&
          // in case of intersecting globs;
          // a path may have been filtered out of this readdir, but
          // shouldn't be removed because it matches a different glob
          (!wh.hasGlob || wh.filterPath({
            fullPath: sysPath.resolve(directory, item)
          }));
      }).forEach(function(item) {
        this._remove(directory, item);
      }, this);
    }.bind(this)).on('error', this._handleError.bind(this));
  }.bind(this);

  var closer;

  if (this.options.depth == null || depth <= this.options.depth) {
    if (!target) read(dir, initialAdd, callback);
    closer = this._watchWithNodeFs(dir, function(dirPath, stats) {
      // if current directory is removed, do nothing
      if (stats && stats.mtime.getTime() === 0) return;

      read(dirPath, false);
    });
  } else {
    callback();
  }
  return closer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._handleError"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleError (error)](#apidoc.element.chokidar.FSWatcher.prototype._handleError)
- description and source-code
```javascript
_handleError = function (error) {
  var code = error && error.code;
  var ipe = this.options.ignorePermissionErrors;
  if (error &&
    code !== 'ENOENT' &&
    code !== 'ENOTDIR' &&
    (!ipe || (code !== 'EPERM' && code !== 'EACCES'))
  ) this.emit('error', error);
  return error || this.closed;
}
```
- example usage
```shell
...
  // don't follow the same symlink more than once
  if (this._symlinkPaths[fullPath]) return;
  else this._symlinkPaths[fullPath] = true;

  this._readyCount++;

  fs.realpath(linkPath, function(error, linkTarget) {
if (this._handleError(error) || this._isIgnored(linkTarget)) {
  return this._emitReady();
}

this._readyCount++;

// add the linkTarget for watching with a wrapper for transform
// that causes emitted paths to incorporate the link's path
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._handleFile"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleFile (file, stats, initialAdd, callback)](#apidoc.element.chokidar.FSWatcher.prototype._handleFile)
- description and source-code
```javascript
_handleFile = function (file, stats, initialAdd, callback) {
  var dirname = sysPath.dirname(file);
  var basename = sysPath.basename(file);
  var parent = this._getWatchedDir(dirname);

  // if the file is already being watched, do nothing
  if (parent.has(basename)) return callback();

  // kick off the watcher
  var closer = this._watchWithNodeFs(file, function(path, newStats) {
    if (!this._throttle('watch', file, 5)) return;
    if (!newStats || newStats && newStats.mtime.getTime() === 0) {
      fs.stat(file, function(error, newStats) {
        // Fix issues where mtime is null but file is still present
        if (error) {
          this._remove(dirname, basename);
        } else {
          this._emit('change', file, newStats);
        }
      }.bind(this));
    // add is about to be emitted if file not already tracked in parent
    } else if (parent.has(basename)) {
      this._emit('change', file, newStats);
    }
  }.bind(this));

  // emit an add event if we're supposed to
  if (!(initialAdd && this.options.ignoreInitial)) {
    if (!this._throttle('add', file, 0)) return;
    this._emit('add', file, stats);
  }

  if (callback) callback();
  return closer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._handleSymlink"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_handleSymlink (entry, directory, path, item)](#apidoc.element.chokidar.FSWatcher.prototype._handleSymlink)
- description and source-code
```javascript
_handleSymlink = function (entry, directory, path, item) {
  var full = entry.fullPath;
  var dir = this._getWatchedDir(directory);

  if (!this.options.followSymlinks) {
    // watch symlink directly (don't follow) and detect changes
    this._readyCount++;
    fs.realpath(path, function(error, linkPath) {
      if (dir.has(item)) {
        if (this._symlinkPaths[full] !== linkPath) {
          this._symlinkPaths[full] = linkPath;
          this._emit('change', path, entry.stat);
        }
      } else {
        dir.add(item);
        this._symlinkPaths[full] = linkPath;
        this._emit('add', path, entry.stat);
      }
      this._emitReady();
    }.bind(this));
    return true;
  }

  // don't follow the same symlink more than once
  if (this._symlinkPaths[full]) return true;
  else this._symlinkPaths[full] = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._hasReadPermissions"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_hasReadPermissions (stats)](#apidoc.element.chokidar.FSWatcher.prototype._hasReadPermissions)
- description and source-code
```javascript
_hasReadPermissions = function (stats) {
  return Boolean(4 & parseInt(((stats && stats.mode) & 0x1ff).toString(8)[0], 10));
}
```
- example usage
```shell
...

var filterPath = function(entry) {
  if (entry.stat && entry.stat.isSymbolicLink()) return filterDir(entry);
  var resolvedPath = entryPath(entry);
  return (!hasGlob || globFilter(resolvedPath)) &&
    this._isntIgnored(resolvedPath, entry.stat) &&
    (this.options.ignorePermissionErrors ||
      this._hasReadPermissions(entry.stat));
}.bind(this);

var getDirParts = function(path) {
  if (!hasGlob) return false;
  var parts = sysPath.relative(watchPath, path).split(/[\/\\]/);
  return parts;
};
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._isIgnored"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_isIgnored (path, stats)](#apidoc.element.chokidar.FSWatcher.prototype._isIgnored)
- description and source-code
```javascript
_isIgnored = function (path, stats) {
  if (this.options.atomic && dotRe.test(path)) return true;

  if (!this._userIgnored) {
    var cwd = this.options.cwd;
    var ignored = this.options.ignored;
    if (cwd && ignored) {
      ignored = ignored.map(function (path) {
        if (typeof path !== 'string') return path;
        return isAbsolute(path) ? path : sysPath.join(cwd, path);
      });
    }
    var paths = arrify(ignored)
      .filter(function(path) {
        return typeof path === 'string' && !isGlob(path);
      }).map(function(path) {
        return path + '/**';
      });
    this._userIgnored = anymatch(
      this._globIgnored.concat(ignored).concat(paths)
    );
  }

  return this._userIgnored([path, stats]);
}
```
- example usage
```shell
...
  if (!awf.pollInterval) awf.pollInterval = 100;

  this._pendingWrites = Object.create(null);
}
if (opts.ignored) opts.ignored = arrify(opts.ignored);

this._isntIgnored = function(path, stat) {
  return !this._isIgnored(path, stat);
}.bind(this);

var readyCalls = 0;
this._emitReady = function() {
  if (++readyCalls >= this._readyCount) {
    this._emitReady = Function.prototype;
    this._readyEmitted = true;
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._remove"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_remove (directory, item)](#apidoc.element.chokidar.FSWatcher.prototype._remove)
- description and source-code
```javascript
_remove = function (directory, item) {
  // if what is being deleted is a directory, get that directory's paths
  // for recursive deleting and cleaning of watched object
  // if it is not a directory, nestedDirectoryChildren will be empty array
  var path = sysPath.join(directory, item);
  var fullPath = sysPath.resolve(path);
  var isDirectory = this._watched[path] || this._watched[fullPath];

  // prevent duplicate handling in case of arriving here nearly simultaneously
  // via multiple paths (such as _handleFile and _handleDir)
  if (!this._throttle('remove', path, 100)) return;

  // if the only watched file is removed, watch for its return
  var watchedDirs = Object.keys(this._watched);
  if (!isDirectory && !this.options.useFsEvents && watchedDirs.length === 1) {
    this.add(directory, item, true);
  }

  // This will create a new entry in the watched object in either case
  // so we got to do the directory check beforehand
  var nestedDirectoryChildren = this._getWatchedDir(path).children();

  // Recursively remove children directories / files.
  nestedDirectoryChildren.forEach(function(nestedItem) {
    this._remove(path, nestedItem);
  }, this);

  // Check if item was on the watched list and remove it
  var parent = this._getWatchedDir(directory);
  var wasTracked = parent.has(item);
  parent.remove(item);

  // If we wait for this file to be fully written, cancel the wait.
  var relPath = path;
  if (this.options.cwd) relPath = sysPath.relative(this.options.cwd, path);
  if (this.options.awaitWriteFinish && this._pendingWrites[relPath]) {
    var event = this._pendingWrites[relPath].cancelWait();
    if (event === 'add') return;
  }

  // The Entry will either be a directory that just got removed
  // or a bogus entry to a file, in either case we have to remove it
  delete this._watched[path];
  delete this._watched[fullPath];
  var eventName = isDirectory ? 'unlinkDir' : 'unlink';
  if (wasTracked && !this._isIgnored(path)) this._emit(eventName, path);

  // Avoid conflicts if we later create another file with the same name
  if (!this.options.useFsEvents) {
    this._closePath(path);
  }
}
```
- example usage
```shell
...

// This will create a new entry in the watched object in either case
// so we got to do the directory check beforehand
var nestedDirectoryChildren = this._getWatchedDir(path).children();

// Recursively remove children directories / files.
nestedDirectoryChildren.forEach(function(nestedItem) {
  this._remove(path, nestedItem);
}, this);

// Check if item was on the watched list and remove it
var parent = this._getWatchedDir(directory);
var wasTracked = parent.has(item);
parent.remove(item);
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._throttle"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_throttle (action, path, timeout)](#apidoc.element.chokidar.FSWatcher.prototype._throttle)
- description and source-code
```javascript
_throttle = function (action, path, timeout) {
  if (!(action in this._throttled)) {
    this._throttled[action] = Object.create(null);
  }
  var throttled = this._throttled[action];
  if (path in throttled) return false;
  function clear() {
    delete throttled[path];
    clearTimeout(timeoutObject);
  }
  var timeoutObject = setTimeout(clear, timeout);
  throttled[path] = {timeoutObject: timeoutObject, clear: clear};
  return throttled[path];
}
```
- example usage
```shell
...
  };

  this._awaitWriteFinish(path, awf.stabilityThreshold, event, awfEmit);
  return this;
}

if (event === 'change') {
  if (!this._throttle('change', path, 50)) return this;
}

if (
  this.options.alwaysStat && val1 === undefined &&
  (event === 'add' || event === 'addDir' || event === 'change')
) {
  var fullPath = this.options.cwd ? sysPath.join(this.options.cwd, path) : path;
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype._watchWithNodeFs"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>_watchWithNodeFs (path, listener)](#apidoc.element.chokidar.FSWatcher.prototype._watchWithNodeFs)
- description and source-code
```javascript
_watchWithNodeFs = function (path, listener) {
  var directory = sysPath.dirname(path);
  var basename = sysPath.basename(path);
  var parent = this._getWatchedDir(directory);
  parent.add(basename);
  var absolutePath = sysPath.resolve(path);
  var options = {persistent: this.options.persistent};
  if (!listener) listener = Function.prototype; // empty function

  var closer;
  if (this.options.usePolling) {
    options.interval = this.enableBinaryInterval && isBinaryPath(basename) ?
      this.options.binaryInterval : this.options.interval;
    closer = setFsWatchFileListener(path, absolutePath, options, {
      listener: listener,
      rawEmitter: this.emit.bind(this, 'raw')
    });
  } else {
    closer = setFsWatchListener(path, absolutePath, options, {
      listener: listener,
      errHandler: this._handleError.bind(this),
      rawEmitter: this.emit.bind(this, 'raw')
    });
  }
  return closer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype.add"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>add (paths, _origAdd, _internal)](#apidoc.element.chokidar.FSWatcher.prototype.add)
- description and source-code
```javascript
add = function (paths, _origAdd, _internal) {
  var cwd = this.options.cwd;
  this.closed = false;
  paths = flatten(arrify(paths));

  if (!paths.every(isString)) {
    throw new TypeError('Non-string provided as watch path: ' + paths);
  }

  if (cwd) paths = paths.map(function(path) {
    if (isAbsolute(path)) {
      return path;
    } else if (path[0] === '!') {
      return '!' + sysPath.join(cwd, path.substring(1));
    } else {
      return sysPath.join(cwd, path);
    }
  });

  // set aside negated glob strings
  paths = paths.filter(function(path) {
    if (path[0] === '!') {
      this._ignoredPaths[path.substring(1)] = true;
    } else {
      // if a path is being added that was previously ignored, stop ignoring it
      delete this._ignoredPaths[path];
      delete this._ignoredPaths[path + '/**'];

      // reset the cached userIgnored anymatch fn
      // to make ignoredPaths changes effective
      this._userIgnored = null;

      return true;
    }
  }, this);

  if (this.options.useFsEvents && FsEventsHandler.canUse()) {
    if (!this._readyCount) this._readyCount = paths.length;
    if (this.options.persistent) this._readyCount *= 2;
    paths.forEach(this._addToFsEvents, this);
  } else {
    if (!this._readyCount) this._readyCount = 0;
    this._readyCount += paths.length;
    asyncEach(paths, function(path, next) {
      this._addToNodeFs(path, !_internal, 0, 0, _origAdd, function(err, res) {
        if (res) this._emitReady();
        next(err, res);
      }.bind(this));
    }.bind(this), function(error, results) {
      results.forEach(function(item) {
        if (!item) return;
        this.add(sysPath.dirname(item), sysPath.basename(_origAdd || item));
      }, this);
    }.bind(this));
  }

  return this;
}
```
- example usage
```shell
...
// 'add', 'addDir' and 'change' events also receive stat() results as second
// argument when available: http://nodejs.org/api/fs.html#fs_class_fs_stats
watcher.on('change', (path, stats) => {
  if (stats) console.log('File ${path} changed size to ${stats.size}');
});

// Watch new files.
watcher.add('new-file');
watcher.add(['new-file-2', 'new-file-3', '**/other-file*']);

// Get list of actual paths being watched on the filesystem
var watchedPaths = watcher.getWatched();

// Un-watch some files.
watcher.unwatch('new-file*');
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype.close"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>close ()](#apidoc.element.chokidar.FSWatcher.prototype.close)
- description and source-code
```javascript
close = function () {
  if (this.closed) return this;

  this.closed = true;
  Object.keys(this._closers).forEach(function(watchPath) {
    this._closers[watchPath]();
    delete this._closers[watchPath];
  }, this);
  this._watched = Object.create(null);

  this.removeAllListeners();
  return this;
}
```
- example usage
```shell
...
// Get list of actual paths being watched on the filesystem
var watchedPaths = watcher.getWatched();

// Un-watch some files.
watcher.unwatch('new-file*');

// Stop watching.
watcher.close();

// Full list of options. See below for descriptions. (do not use this example)
chokidar.watch('file', {
persistent: true,

ignored: '*.txt',
ignoreInitial: false,
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype.getWatched"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>getWatched ()](#apidoc.element.chokidar.FSWatcher.prototype.getWatched)
- description and source-code
```javascript
getWatched = function () {
  var watchList = {};
  Object.keys(this._watched).forEach(function(dir) {
    var key = this.options.cwd ? sysPath.relative(this.options.cwd, dir) : dir;
    watchList[key || '.'] = Object.keys(this._watched[dir]._items).sort();
  }.bind(this));
  return watchList;
}
```
- example usage
```shell
...
});

// Watch new files.
watcher.add('new-file');
watcher.add(['new-file-2', 'new-file-3', '**/other-file*']);

// Get list of actual paths being watched on the filesystem
var watchedPaths = watcher.getWatched();

// Un-watch some files.
watcher.unwatch('new-file*');

// Stop watching.
watcher.close();
...
```

#### <a name="apidoc.element.chokidar.FSWatcher.prototype.unwatch"></a>[function <span class="apidocSignatureSpan">chokidar.FSWatcher.prototype.</span>unwatch (paths)](#apidoc.element.chokidar.FSWatcher.prototype.unwatch)
- description and source-code
```javascript
unwatch = function (paths) {
  if (this.closed) return this;
  paths = flatten(arrify(paths));

  paths.forEach(function(path) {
    // convert to absolute path unless relative path already matches
    if (!isAbsolute(path) && !this._closers[path]) {
      if (this.options.cwd) path = sysPath.join(this.options.cwd, path);
      path = sysPath.resolve(path);
    }

    this._closePath(path);

    this._ignoredPaths[path] = true;
    if (path in this._watched) {
      this._ignoredPaths[path + '/**'] = true;
    }

    // reset the cached userIgnored anymatch fn
    // to make ignoredPaths changes effective
    this._userIgnored = null;
  }, this);

  return this;
}
```
- example usage
```shell
...
watcher.add('new-file');
watcher.add(['new-file-2', 'new-file-3', '**/other-file*']);

// Get list of actual paths being watched on the filesystem
var watchedPaths = watcher.getWatched();

// Un-watch some files.
watcher.unwatch('new-file*');

// Stop watching.
watcher.close();

// Full list of options. See below for descriptions. (do not use this example)
chokidar.watch('file', {
persistent: true,
...
```



# <a name="apidoc.module.chokidar.fsevents_handler"></a>[module chokidar.fsevents_handler](#apidoc.module.chokidar.fsevents_handler)

#### <a name="apidoc.element.chokidar.fsevents_handler.fsevents_handler"></a>[function <span class="apidocSignatureSpan">chokidar.</span>fsevents_handler ()](#apidoc.element.chokidar.fsevents_handler.fsevents_handler)
- description and source-code
```javascript
function FsEventsHandler() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.chokidar.fsevents_handler.canUse"></a>[function <span class="apidocSignatureSpan">chokidar.fsevents_handler.</span>canUse ()](#apidoc.element.chokidar.fsevents_handler.canUse)
- description and source-code
```javascript
function canUse() {
  return fsevents && Object.keys(FSEventsWatchers).length < 128;
}
```
- example usage
```shell
...
if (undef('binaryInterval')) opts.binaryInterval = 300;
this.enableBinaryInterval = opts.binaryInterval !== opts.interval;

// Enable fsevents on OS X when polling isn't explicitly enabled.
if (undef('useFsEvents')) opts.useFsEvents = !opts.usePolling;

// If we can't use fsevents, ensure the options reflect it's disabled.
if (!FsEventsHandler.canUse()) opts.useFsEvents = false;

// Use polling on Mac if not using fsevents.
// Other platforms use non-polling fs.watch.
if (undef('usePolling') && !opts.useFsEvents) {
  opts.usePolling = process.platform === 'darwin';
}
...
```



# <a name="apidoc.module.chokidar.fsevents_handler.prototype"></a>[module chokidar.fsevents_handler.prototype](#apidoc.module.chokidar.fsevents_handler.prototype)

#### <a name="apidoc.element.chokidar.fsevents_handler.prototype._addToFsEvents"></a>[function <span class="apidocSignatureSpan">chokidar.fsevents_handler.prototype.</span>_addToFsEvents (path, transform, forceAdd, priorDepth)](#apidoc.element.chokidar.fsevents_handler.prototype._addToFsEvents)
- description and source-code
```javascript
_addToFsEvents = function (path, transform, forceAdd, priorDepth) {

  // applies transform if provided, otherwise returns same value
  var processPath = typeof transform === 'function' ?
    transform : function(val) { return val; };

  var emitAdd = function(newPath, stats) {
    var pp = processPath(newPath);
    var isDir = stats.isDirectory();
    var dirObj = this._getWatchedDir(sysPath.dirname(pp));
    var base = sysPath.basename(pp);

    // ensure empty dirs get tracked
    if (isDir) this._getWatchedDir(pp);

    if (dirObj.has(base)) return;
    dirObj.add(base);

    if (!this.options.ignoreInitial || forceAdd === true) {
      this._emit(isDir ? 'addDir' : 'add', pp, stats);
    }
  }.bind(this);

  var wh = this._getWatchHelpers(path);

  // evaluate what is at the path we're being asked to watch
  fs[wh.statMethod](wh.watchPath, function(error, stats) {
    if (this._handleError(error) || this._isIgnored(wh.watchPath, stats)) {
      this._emitReady();
      return this._emitReady();
    }

    if (stats.isDirectory()) {
      // emit addDir unless this is a glob parent
      if (!wh.globFilter) emitAdd(processPath(path), stats);

      // don't recurse further if it would exceed depth setting
      if (priorDepth && priorDepth > this.options.depth) return;

      // scan the contents of the dir
      readdirp({
        root: wh.watchPath,
        entryType: 'all',
        fileFilter: wh.filterPath,
        directoryFilter: wh.filterDir,
        lstat: true,
        depth: this.options.depth - (priorDepth || 0)
      }).on('data', function(entry) {
        // need to check filterPath on dirs b/c filterDir is less restrictive
        if (entry.stat.isDirectory() && !wh.filterPath(entry)) return;

        var joinedPath = sysPath.join(wh.watchPath, entry.path);
        var fullPath = entry.fullPath;

        if (wh.followSymlinks && entry.stat.isSymbolicLink()) {
          // preserve the current depth here since it can't be derived from
          // real paths past the symlink
          var curDepth = this.options.depth === undefined ?
            undefined : depth(joinedPath, sysPath.resolve(wh.watchPath)) + 1;

          this._handleFsEventsSymlink(joinedPath, fullPath, processPath, curDepth);
        } else {
          emitAdd(joinedPath, entry.stat);
        }
      }.bind(this)).on('error', function() {
        // Ignore readdirp errors
      }).on('end', this._emitReady);
    } else {
      emitAdd(wh.watchPath, stats);
      this._emitReady();
    }
  }.bind(this));

  if (this.options.persistent && forceAdd !== true) {
    var initWatch = function(error, realPath) {
      var closer = this._watchWithFsEvents(
        wh.watchPath,
        sysPath.resolve(realPath || wh.watchPath),
        processPath,
        wh.globFilter
      );
      if (closer) this._closers[path] = closer;
    }.bind(this);

    if (typeof transform === 'function') {
      // realpath has already been resolved
      initWatch();
    } else {
      fs.realpath(wh.watchPath, initWatch);
    }
  }
}
```
- example usage
```shell
...
  // track new directories
  if (info.type === 'directory') this._getWatchedDir(path);

  if (info.type === 'symlink' && this.options.followSymlinks) {
    // push symlinks back to the top of the stack to get handled
    var curDepth = this.options.depth === undefined ?
      undefined : depth(fullPath, realPath) + 1;
    return this._addToFsEvents(path, false, true, curDepth);
  } else {
    // track new paths
    // (other than symlinks being followed, which will be tracked soon)
    this._getWatchedDir(parent).add(item);
  }
}
var eventName = info.type === 'directory' ? event + 'Dir' : event;
...
```

#### <a name="apidoc.element.chokidar.fsevents_handler.prototype._handleFsEventsSymlink"></a>[function <span class="apidocSignatureSpan">chokidar.fsevents_handler.prototype.</span>_handleFsEventsSymlink (linkPath, fullPath, transform, curDepth)](#apidoc.element.chokidar.fsevents_handler.prototype._handleFsEventsSymlink)
- description and source-code
```javascript
_handleFsEventsSymlink = function (linkPath, fullPath, transform, curDepth) {
  // don't follow the same symlink more than once
  if (this._symlinkPaths[fullPath]) return;
  else this._symlinkPaths[fullPath] = true;

  this._readyCount++;

  fs.realpath(linkPath, function(error, linkTarget) {
    if (this._handleError(error) || this._isIgnored(linkTarget)) {
      return this._emitReady();
    }

    this._readyCount++;

    // add the linkTarget for watching with a wrapper for transform
    // that causes emitted paths to incorporate the link's path
    this._addToFsEvents(linkTarget || linkPath, function(path) {
      var dotSlash = '.' + sysPath.sep;
      var aliasedPath = linkPath;
      if (linkTarget && linkTarget !== dotSlash) {
        aliasedPath = path.replace(linkTarget, linkPath);
      } else if (path !== dotSlash) {
        aliasedPath = sysPath.join(linkPath, path);
      }
      return transform(aliasedPath);
    }, false, curDepth);
  }.bind(this));
}
```
- example usage
```shell
...

    if (wh.followSymlinks && entry.stat.isSymbolicLink()) {
      // preserve the current depth here since it can't be derived from
      // real paths past the symlink
      var curDepth = this.options.depth === undefined ?
        undefined : depth(joinedPath, sysPath.resolve(wh.watchPath)) + 1;

      this._handleFsEventsSymlink(joinedPath, fullPath, processPath, curDepth);
    } else {
      emitAdd(joinedPath, entry.stat);
    }
  }.bind(this)).on('error', function() {
    // Ignore readdirp errors
  }).on('end', this._emitReady);
} else {
...
```

#### <a name="apidoc.element.chokidar.fsevents_handler.prototype._watchWithFsEvents"></a>[function <span class="apidocSignatureSpan">chokidar.fsevents_handler.prototype.</span>_watchWithFsEvents (watchPath, realPath, transform, globFilter)](#apidoc.element.chokidar.fsevents_handler.prototype._watchWithFsEvents)
- description and source-code
```javascript
_watchWithFsEvents = function (watchPath, realPath, transform, globFilter) {
  if (this._isIgnored(watchPath)) return;
  var watchCallback = function(fullPath, flags, info) {
    if (
      this.options.depth !== undefined &&
      depth(fullPath, realPath) > this.options.depth
    ) return;
    var path = transform(sysPath.join(
      watchPath, sysPath.relative(watchPath, fullPath)
    ));
    if (globFilter && !globFilter(path)) return;
    // ensure directories are tracked
    var parent = sysPath.dirname(path);
    var item = sysPath.basename(path);
    var watchedDir = this._getWatchedDir(
      info.type === 'directory' ? path : parent
    );
    var checkIgnored = function(stats) {
      if (this._isIgnored(path, stats)) {
        this._ignoredPaths[path] = true;
        if (stats && stats.isDirectory()) {
          this._ignoredPaths[path + '/**/*'] = true;
        }
        return true;
      } else {
        delete this._ignoredPaths[path];
        delete this._ignoredPaths[path + '/**/*'];
      }
    }.bind(this);

    var handleEvent = function(event) {
      if (checkIgnored()) return;

      if (event === 'unlink') {
        // suppress unlink events on never before seen files
        if (info.type === 'directory' || watchedDir.has(item)) {
          this._remove(parent, item);
        }
      } else {
        if (event === 'add') {
          // track new directories
          if (info.type === 'directory') this._getWatchedDir(path);

          if (info.type === 'symlink' && this.options.followSymlinks) {
            // push symlinks back to the top of the stack to get handled
            var curDepth = this.options.depth === undefined ?
              undefined : depth(fullPath, realPath) + 1;
            return this._addToFsEvents(path, false, true, curDepth);
          } else {
            // track new paths
            // (other than symlinks being followed, which will be tracked soon)
            this._getWatchedDir(parent).add(item);
          }
        }
        var eventName = info.type === 'directory' ? event + 'Dir' : event;
        this._emit(eventName, path);
        if (eventName === 'addDir') this._addToFsEvents(path, false, true);
      }
    }.bind(this);

    function addOrChange() {
      handleEvent(watchedDir.has(item) ? 'change' : 'add');
    }
    function checkFd() {
      fs.open(path, 'r', function(error, fd) {
        if (fd) fs.close(fd);
        error && error.code !== 'EACCES' ?
          handleEvent('unlink') : addOrChange();
      });
    }
    // correct for wrong events emitted
    var wrongEventFlags = [
      69888, 70400, 71424, 72704, 73472, 131328, 131840, 262912
    ];
    if (wrongEventFlags.indexOf(flags) !== -1 || info.event === 'unknown') {
      if (typeof this.options.ignored === 'function') {
        fs.stat(path, function(error, stats) {
          if (checkIgnored(stats)) return;
          stats ? addOrChange() : handleEvent('unlink');
        });
      } else {
        checkFd();
      }
    } else {
      switch (info.event) {
      case 'created':
      case 'modified':
        return addOrChange();
      case 'deleted':
      case 'moved':
        return checkFd();
      }
    }
  }.bind(this);

  var closer = setFSEventsListener(
    watchPath,
    realPath,
    watchCallback,
    this.emit.bind(this, 'raw')
  );

  this._emitReady();
  return closer;
}
```
- example usage
```shell
...
    emitAdd(wh.watchPath, stats);
    this._emitReady();
  }
}.bind(this));

if (this.options.persistent && forceAdd !== true) {
  var initWatch = function(error, realPath) {
    var closer = this._watchWithFsEvents(
      wh.watchPath,
      sysPath.resolve(realPath || wh.watchPath),
      processPath,
      wh.globFilter
    );
    if (closer) this._closers[path] = closer;
  }.bind(this);
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
