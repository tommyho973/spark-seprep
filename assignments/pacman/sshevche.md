## **podman logs pacman Output**
### *by Sviat*

### Screenshot

![pacman](https://github.com/sshevche-cell/spark-seprep/assets/125435823/b43ceeca-f909-4ccc-9dd4-2fbae117d1cc)

### Output

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



## Extra Code and Output

### Code 

(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 ~ % cd github
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 github % ls
spark-seprep
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 github % cd spark-seprep
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 spark-seprep % ls
LICENSE			Team14_Lucy_Tommy	joke.sh
README.md		assignments		mongo-pacman
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 spark-seprep % cd mong-pacman
cd: no such file or directory: mong-pacman
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 spark-seprep % cd mongo-pacman
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % cd frontend
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 frontend % podman build -t docker.io/sshevche-cell/pacman:latest -f docker/Dockerfile .
STEP 1/10: FROM registry.access.redhat.com/ubi8/ubi
STEP 2/10: WORKDIR /pacman 
--> Using cache 0aa22be7d95df23ab9acf8d8c1cbf0b6dba5a5529ea3170203c8c12d02443db6
--> 0aa22be7d95d
STEP 3/10: RUN dnf -y  module install nodejs:18/common 
--> Using cache 091bd840d634df73b755df3297013b888bef1b22f8eb70069a8e4ed50c8c5137
--> 091bd840d634
STEP 4/10: RUN dnf -y install npm jq  && dnf clean all && npm install mongodb    
--> Using cache cc9257e0eca3fc74ace7a05be50b41400b7016c87fb9a80785f4bf9d929c4ad3
--> cc9257e0eca3
STEP 5/10: COPY . /pacman  
--> Using cache b901ab6b7eabe5637b3765cbb76fa7ce1169faa2ea00acab70e372d6d41565b7
--> b901ab6b7eab
STEP 6/10: RUN chmod -R 777  /pacman
--> Using cache bc64b9bf9a406e889dbfae6317d8dc36b2898ae7a5dbc4f7f72275cb3774b532
--> bc64b9bf9a40
STEP 7/10: RUN npm install 
--> Using cache 12142a3aaffdc93f83edc617f465fb4e37ae6539843a10ba3ddb3781b7d59e2d
--> 12142a3aaffd
STEP 8/10: EXPOSE 8080 
--> Using cache b0e34e13f7907d0f5c2beb22dab30031f45ae139bc12120edaec7122358d7156
--> b0e34e13f790
STEP 9/10: COPY  pacman.sh /usr/local/bin/
--> Using cache 09b5afb573e56cb0d1c4fa32994bd450ece46ca956b26b055d2f49a9ada0ba00
--> 09b5afb573e5
STEP 10/10: ENTRYPOINT ["pacman.sh"]
--> Using cache 8b4cac15b8dc3c14ff223a302dd535fff08a25af93daf528440a5387ac611a26
COMMIT docker.io/sshevche-cell/pacman:latest
--> 8b4cac15b8dc
Successfully tagged docker.io/sshevche-cell/pacman:latest
Successfully tagged docker.io/yourname/pacman:latest
8b4cac15b8dc3c14ff223a302dd535fff08a25af93daf528440a5387ac611a26
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 frontend % cd ../
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % git switch pacman
Already on 'pacman'
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % podman build -t docker.io/sshevche-cell//pacman:latest -f windows-containerfile .
Error: tag docker.io/sshevche-cell//pacman:latest: invalid reference format

(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % podman build -t docker.io/sshevche-cell/pacman:latest -f windows-containerfile .
Error: stat /var/tmp/libpod_builder2324500439/build/windows-containerfile: no such file or directory

(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % podman run --rm -d -it --sshevche-cell pacman -p 8080:8080 docker.io/yourname/pacman:latest
Error: unknown flag: --sshevche-cell
See 'podman run --help'
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % podman run --rm -d -it --name pacman -p 8080:8080 docker.io/sshevche-cell/pacman:latest
Error: creating container storage: the container name "pacman" is already in use by 35be218eb74d784346a520bf3c3526adba0fc0cdd30f6787c15854bc000f651c. You have to remove that container to be able to reuse that name: that name is already in use
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % podman logs pacman


### Output

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
PACMAN: Failed to connect to database server
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % git add .
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % git commit -m "Sviatoslav: Container Images Assignment"
On branch pacman
nothing to commit, working tree clean
(base) sviatshevchenko@crc-dot1x-nat-10-239-97-168 mongo-pacman % git push origin main
To github.com:sshevche-cell/mongo-pacman.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:sshevche-cell/mongo-pacman.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
