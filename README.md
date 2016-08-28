# AirborneSwarm
- rolling-spiderのswarm APIを使って, droneを同時操作するスクリプト
- rolling-spider/lib/swarm.jsの78-79行目を以下のように書き換える
```javascript
    var localNameMatch = localName
      && (localName.indexOf('RS_') === 0 || localName.indexOf('Mars_') === 0 || localName.indexOf('Travis_') === 0  || localName.indexOf('Maclan_')=== 0);
    var manufacturerMatch = manufacturer
      && (['4300cf1900090100', '4300cf1909090100', '4300cf1907090100'].indexOf(manufacturer) >= 0);
```
- droneのIDはconfig.jsonに指定する