NODE VERSION:
v18.18.2
NPM  VERSION:
9.8.1
run pacman
PACMAN auth_details =  pacman:pacman@
DATABASE URL  mongodb://pacman:pacman@mongodb:27017/pacman
CONNECTING  mongodb://pacman:pacman@mongodb:27017/pacman
Options  { readPreference: [32m'secondaryPreferred'[39m }
Listening on port 8080
Time:  Wed Oct 25 2023 22:53:50 GMT+0000 (Coordinated Universal Time)
[GET /loc/metadata]
[getHost]
HOST: 2f01e2151b9c
getCloudMetadata
getK8sCloudMetadata
Querying undefined for cloud data
Error: ENOENT: no such file or directory, open '/var/run/secrets/kubernetes.io/serviceaccount/token'
[90m    at Object.openSync (node:fs:603:3)[39m
[90m    at Object.readFileSync (node:fs:471:35)[39m
    at getK8sCloudMetadata [90m(/pacman/[39mroutes/location.js:347:27[90m)[39m
    at getCloudMetadata [90m(/pacman/[39mroutes/location.js:32:5[90m)[39m
    at [90m/pacman/[39mroutes/location.js:17:5
    at Layer.handle [as handle_request] [90m(/pacman/[39mnode_modules/[4mexpress[24m/lib/router/layer.js:95:5[90m)[39m
    at next [90m(/pacman/[39mnode_modules/[4mexpress[24m/lib/router/route.js:144:13[90m)[39m
    at Route.dispatch [90m(/pacman/[39mnode_modules/[4mexpress[24m/lib/router/route.js:114:3[90m)[39m
    at Layer.handle [as handle_request] [90m(/pacman/[39mnode_modules/[4mexpress[24m/lib/router/layer.js:95:5[90m)[39m
    at [90m/pacman/[39mnode_modules/[4mexpress[24m/lib/router/index.js:284:15 {
  errno: [33m-2[39m,
  syscall: [32m'open'[39m,
  code: [32m'ENOENT'[39m,
  path: [32m'/var/run/secrets/kubernetes.io/serviceaccount/token'[39m
}
Time:  Wed Oct 25 2023 22:53:51 GMT+0000 (Coordinated Universal Time)
[GET /user/id]
getDb:  [1mnull[22m
getDb: Attempting Reconnect !
CONNECTING  mongodb://pacman:pacman@mongodb:27017/pacman
Options  { readPreference: [32m'secondaryPreferred'[39m }
problem with request: getaddrinfo ENOTFOUND kubernetes.default.svc
getAWSCloudMetadata
problem with request: connect ECONNREFUSED 169.254.169.254:80
getAzureCloudMetadata
problem with request: connect ECONNREFUSED 169.254.169.254:80
getGCPCloudMetadata
problem with request: getaddrinfo ENOTFOUND metadata.google.internal
getOpenStackCloudMetadata
problem with request: connect ECONNREFUSED 169.254.169.254:80
CLOUD: unknown
ZONE: unknown
HOST: 2f01e2151b9c
MongoServerSelectionError: getaddrinfo ENOTFOUND mongodb
    at Timeout._onTimeout [90m(/pacman/[39mnode_modules/[4mmongodb[24m/lib/sdam/topology.js:292:38[90m)[39m
[90m    at listOnTimeout (node:internal/timers:569:17)[39m
[90m    at process.processTimers (node:internal/timers:512:7)[39m {
  reason: TopologyDescription {
    type: [32m'Unknown'[39m,
    servers: Map(1) { [32m'mongodb:27017'[39m => [36m[ServerDescription][39m },
    stale: [33mfalse[39m,
    compatible: [33mtrue[39m,
    heartbeatFrequencyMS: [33m10000[39m,
    localThresholdMS: [33m15[39m,
    setName: [1mnull[22m,
    maxElectionId: [1mnull[22m,
    maxSetVersion: [1mnull[22m,
    commonWireVersion: [33m0[39m,
    logicalSessionTimeoutMinutes: [1mnull[22m
  },
  code: [90mundefined[39m,
  [[32mSymbol(errorLabels)[39m]: Set(0) {}
}
mongodb://pacman:pacman@mongodb:27017/pacman
{ readPreference: [32m'secondaryPreferred'[39m }
PACMAN: Failed to connect to database server
MongoServerSelectionError: getaddrinfo ENOTFOUND mongodb
    at Timeout._onTimeout [90m(/pacman/[39mnode_modules/[4mmongodb[24m/lib/sdam/topology.js:292:38[90m)[39m
[90m    at listOnTimeout (node:internal/timers:569:17)[39m
[90m    at process.processTimers (node:internal/timers:512:7)[39m {
  reason: TopologyDescription {
    type: [32m'Unknown'[39m,
    servers: Map(1) { [32m'mongodb:27017'[39m => [36m[ServerDescription][39m },
    stale: [33mfalse[39m,
    compatible: [33mtrue[39m,
    heartbeatFrequencyMS: [33m10000[39m,
    localThresholdMS: [33m15[39m,
    setName: [1mnull[22m,
    maxElectionId: [1mnull[22m,
    maxSetVersion: [1mnull[22m,
    commonWireVersion: [33m0[39m,
    logicalSessionTimeoutMinutes: [1mnull[22m
  },
  code: [90mundefined[39m,
  [[32mSymbol(errorLabels)[39m]: Set(0) {}
}
mongodb://pacman:pacman@mongodb:27017/pacman
{ readPreference: [32m'secondaryPreferred'[39m }
getDb: Failed to connect to database server
