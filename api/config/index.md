---
layout: default
menu_item: api
title: Config
description: Version 0.19.0
menu_item: api
return_to:
  "API Documentation Index": /api/
sections:
  "findProgramdata": "#findProgramdata"
  "openDefault": "#openDefault"
  "#getStringBuf": "#getStringBuf"
  "#lock": "#lock"
  "#setInt64": "#setInt64"
  "#setMultivar": "#setMultivar"
  "#setString": "#setString"
  "#snapshot": "#snapshot"
  "LEVEL": "#LEVEL"
---

## <a name="findProgramdata"></a><span>Config.</span>findProgramdata <span class="tags"><span class="async">Async</span></span>

```js
Config.findProgramdata().then(function(buf) {
  // Use buf
});
```

| Returns |  |
| --- | --- |
| [Buf](/api/buf/) |  |

## <a name="openDefault"></a><span>Config.</span>openDefault <span class="tags"><span class="async">Async</span></span>

```js
Config.openDefault().then(function(config) {
  // Use config
});
```

| Returns |  |
| --- | --- |
| [Config](/api/config/) |  |

## <a name="getStringBuf"></a><span>Config#</span>getStringBuf <span class="tags"><span class="async">Async</span></span>

```js
config.getStringBuf(name).then(function(buf) {
  // Use buf
});
```

| Parameters | Type |
| --- | --- | --- |
| name | String | the variable's name |

| Returns |  |
| --- | --- |
| [Buf](/api/buf/) | buffer in which to store the string |

## <a name="lock"></a><span>Config#</span>lock <span class="tags"><span class="sync">Sync</span></span>

```js
var result = config.lock(tx);
```

| Parameters | Type |
| --- | --- | --- |
| tx | [Transaction](/api/transaction/) | the resulting transaction, use this to commit or undo the changes |

| Returns |  |
| --- | --- |
| Number |  0 or an error code |

## <a name="setInt64"></a><span>Config#</span>setInt64 <span class="tags"><span class="sync">Sync</span></span>

```js
var result = config.setInt64(name, value);
```

| Parameters | Type |
| --- | --- | --- |
| name | String | the variable's name |
| value | Number | Long integer value for the variable |

| Returns |  |
| --- | --- |
| Number |  0 or an error code |

## <a name="setMultivar"></a><span>Config#</span>setMultivar <span class="tags"><span class="sync">Sync</span></span>

```js
var result = config.setMultivar(name, regexp, value);
```

| Parameters | Type |
| --- | --- | --- |
| name | String | the variable's name |
| regexp | String | a regular expression to indicate which values to replace |
| value | String | the new value. |

| Returns |  |
| --- | --- |
| Number |  |

## <a name="setString"></a><span>Config#</span>setString <span class="tags"><span class="async">Async</span></span>

```js
config.setString(name, value).then(function(result) {
  // Use result
});
```

| Parameters | Type |
| --- | --- | --- |
| name | String | the variable's name |
| value | String | the string to store. |

| Returns |  |
| --- | --- |
| Number |  0 or an error code |

## <a name="snapshot"></a><span>Config#</span>snapshot <span class="tags"><span class="async">Async</span></span>

```js
config.snapshot().then(function(config) {
  // Use config
});
```

| Returns |  |
| --- | --- |
| [Config](/api/config/) |  |

## <a name="LEVEL"></a><span>Config.</span>LEVEL <span class="tags"><span class="enum">ENUM</span></span>

| Flag | Value |
| --- | --- | --- |
| <span>Config.LEVEL.</span>PROGRAMDATA | 1 |
| <span>Config.LEVEL.</span>SYSTEM | 2 |
| <span>Config.LEVEL.</span>XDG | 3 |
| <span>Config.LEVEL.</span>GLOBAL | 4 |
| <span>Config.LEVEL.</span>LOCAL | 5 |
| <span>Config.LEVEL.</span>APP | 6 |
| <span>Config.LEVEL.</span>HIGHEST_LEVEL | -1 |

