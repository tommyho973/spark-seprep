(base) namannagaria@crc-dot1x-nat-10-239-40-17 mongo-pacman % podman logs pacman
NODE VERSION:
v18.18.2
NPM  VERSION:
9.8.1
run pacman
PACMAN auth_details =  pacman:pacman@
DATABASE URL  mongodb://pacman:pacman@mongodb:27017/pacman
CONNECTING  mongodb://pacman:pacman@mongodb:27017/pacman
Options  { readPreference: 'secondaryPreferred' }
Listening on port 8080
MongoServerSelectionError: getaddrinfo ENOTFOUND mongodb
    at Timeout._onTimeout (/pacman/node_modules/mongodb/lib/sdam/topology.js:292:38)
    at listOnTimeout (node:internal/timers:569:17)
    at process.processTimers (node:internal/timers:512:7) {
  reason: TopologyDescription {
    type: 'Unknown',
    servers: Map(1) { 'mongodb:27017' => [ServerDescription] },
    stale: false,
    compatible: true,
    heartbeatFrequencyMS: 10000,
    localThresholdMS: 15,
    setName: null,
    maxElectionId: null,
    maxSetVersion: null,
    commonWireVersion: 0,
    logicalSessionTimeoutMinutes: null
  },
  code: undefined,
  [Symbol(errorLabels)]: Set(0) {}
}
mongodb://pacman:pacman@mongodb:27017/pacman
{ readPreference: 'secondaryPreferred' }
PACMAN: Failed to connect to database server```markdown
(base) namannagaria@crc-dot1x-nat-10-239-40-17 mongo-pacman % podman logs pacman

**NODE VERSION:**
v18.18.2

**NPM VERSION:**
9.8.1

run pacman

**PACMAN auth_details =**  pacman:pacman@

**DATABASE URL**  `mongodb://pacman:pacman@mongodb:27017/pacman`

**CONNECTING**  `mongodb://pacman:pacman@mongodb:27017/pacman`

**Options:**  `{ readPreference: 'secondaryPreferred' }`

**Listening on port 8080**

**MongoServerSelectionError:** `getaddrinfo ENOTFOUND mongodb`
   - **reason:** TopologyDescription {
      type: 'Unknown',
      servers: Map(1) { 'mongodb:27017' => [ServerDescription] },
      stale: false,
      compatible: true,
      heartbeatFrequencyMS: 10000,
      localThresholdMS: 15,
      setName: null,
      maxElectionId: null,
      maxSetVersion: null,
      commonWireVersion: 0,
      logicalSessionTimeoutMinutes: null
   },
   - **code:** undefined

`mongodb://pacman:pacman@mongodb:27017/pacman`
{ readPreference: 'secondaryPreferred' }

**PACMAN:** Failed to connect to the database server

**Time:** Sat Nov 04 2023 21:12:44 GMT+0000 (Coordinated Universal Time)

[GET /loc/metadata]
[getHost]
**HOST:** c710a082ab1e

**getCloudMetadata**
**getK8sCloudMetadata**
   - Querying undefined for cloud data

**Error:** ENOENT: no such file or directory, open '/var/run/secrets/kubernetes.io/serviceaccount/token'
   - at Object.openSync (node:fs:603:3)
   - at Object.readFileSync (node:fs:471:35)
   - at getK8sCloudMetadata (/pacman/routes/location.js:347:27)
   - at getCloudMetadata (/pacman/routes/location.js:32:5)
   - at /pacman/routes/location.js:17:5

**problem with request:** `getaddrinfo ENOTFOUND kubernetes.default.svc`

**getAWSCloudMetadata**
**problem with request:** `connect ECONNREFUSED 169.254.169.254:80`

**getAzureCloudMetadata**
**problem with request:** `connect ECONNREFUSED 169.254.169.254:80`

**getGCPCloudMetadata**
**problem with request:** `getaddrinfo ENOTFOUND metadata.google.internal`

**getOpenStackCloudMetadata**
**problem with request:** `connect ECONNREFUSED 169.254.169.254:80`

**CLOUD:** unknown
**ZONE:** unknown
**HOST:** c710a082ab1e

**Time:** Sat Nov 04 2023 21:12:47 GMT+0000 (Coordinated Universal Time)

[GET /user/id]

**getDb:**  null

**getDb:** Attempting Reconnect !

**CONNECTING**  `mongodb://pacman:pacman@mongodb:27017/pacman`

**Options:**  `{ readPreference: 'secondaryPreferred' }`

**MongoServerSelectionError:** `getaddrinfo ENOTFOUND mongodb`
   - **reason:** TopologyDescription {
      type: 'Unknown',
      servers: Map(1) { 'mongodb:27017' => [ServerDescription] },
      stale: false,
      compatible: true,
      heartbeatFrequencyMS: 10000,
      localThresholdMS: 15,
      setName: null,
      maxElectionId: null,
      maxSetVersion: null,
      commonWireVersion: 0,
      logicalSessionTimeoutMinutes: null
   },
   - **code:** undefined

`mongodb://pacman:pacman@mongodb:27017/pacman`
{ readPreference: 'secondaryPreferred' }

**getDb:** Failed to connect to the database server
```markdown

Time:  Sat Nov 04 2023 21:12:44 GMT+0000 (Coordinated Universal Time)
[GET /loc/metadata]
[getHost]
HOST: c710a082ab1e
getCloudMetadata
getK8sCloudMetadata
Querying undefined for cloud data
Error: ENOENT: no such file or directory, open '/var/run/secrets/kubernetes.io/serviceaccount/token'
    at Object.openSync (node:fs:603:3)
    at Object.readFileSync (node:fs:471:35)
    at getK8sCloudMetadata (/pacman/routes/location.js:347:27)
    at getCloudMetadata (/pacman/routes/location.js:32:5)
    at /pacman/routes/location.js:17:5
    at Layer.handle [as handle_request] (/pacman/node_modules/express/lib/router/layer.js:95:5)
    at next (/pacman/node_modules/express/lib/router/route.js:144:13)
    at Route.dispatch (/pacman/node_modules/express/lib/router/route.js:114:3)
    at Layer.handle [as handle_request] (/pacman/node_modules/express/lib/router/layer.js:95:5)
    at /pacman/node_modules/express/lib/router/index.js:284:15 {
  errno: -2,
  syscall: 'open',
  code: 'ENOENT',
  path: '/var/run/secrets/kubernetes.io/serviceaccount/token'
}
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
HOST: c710a082ab1e
Time:  Sat Nov 04 2023 21:12:47 GMT+0000 (Coordinated Universal Time)
[GET /user/id]
getDb:  null
getDb: Attempting Reconnect !
CONNECTING  mongodb://pacman:pacman@mongodb:27017/pacman
Options  { readPreference: 'secondaryPreferred' }
MongoServerSelectionError: getaddrinfo ENOTFOUND mongodb
    at Timeout._onTimeout (/pacman/node_modules/mongodb/lib/sdam/topology.js:292:38)
    at listOnTimeout (node:internal/timers:569:17)
    at process.processTimers (node:internal/timers:512:7) {
  reason: TopologyDescription {
    type: 'Unknown',
    servers: Map(1) { 'mongodb:27017' => [ServerDescription] },
    stale: false,
    compatible: true,
    heartbeatFrequencyMS: 10000,
    localThresholdMS: 15,
    setName: null,
    maxElectionId: null,
    maxSetVersion: null,
    commonWireVersion: 0,
    logicalSessionTimeoutMinutes: null
  },
  code: undefined,
  [Symbol(errorLabels)]: Set(0) {}
}
mongodb://pacman:pacman@mongodb:27017/pacman
{ readPreference: 'secondaryPreferred' }
getDb: Failed to connect to database server




**I faced a lot of trouble in this assigment, from podman not working to reinstalling macOS. I know i am late for this assigment but I tried to add markdown to this for extra credit.**
