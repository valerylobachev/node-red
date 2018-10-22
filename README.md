# Node-RED with Keycloak authentication



## Getting started

If you want to run the latest code from git, here's how to get started:

1. Clone the code:

        git clone https://github.com/valerylobachev/node-red.git
        cd node-red

2. Install the node-red dependencies

        npm install

3. Build the code

        npm run build

4. Install runtime dependencies
        
        cd ~
        mkdir .node-red
        cd .node-red
        npm install @exlinc/keycloak-passport --save
        cd <node-red path>
        
5. Install & configure Keycloak:  

 * Download & install Keycloak according [installation guide](https://www.keycloak.org/docs/latest/server_installation/index.html) 
 * Run Keycloak
        
        ./bin/standalone.sh -Djboss.socket.binding.port-offset=100
   
 * Open Keycloak's administration console [http://localhost:8180/auth/admin/](http://localhost:8180/auth/admin/)       
 * Create realm Annette using `keycloak\realm.json`
 * Create users in new realm
 
6. Run

        npm start
   or

        node red.js



## Copyright and license

Copyright JS Foundation and other contributors, http://js.foundation under [the Apache 2.0 license](LICENSE).
