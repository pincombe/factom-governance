# Testnet Directions

Testnet Directions for docker swarm

Install docker on your test machine

  - > If a previous factomd docker is running, stop it from running.
    
      - > \`docker ps\`
    
      - > \`docker stop \<container ID\>
    
      - > If you followed the standard install procedure change to
        > factom/communitytestnet and run \`docker-compose down\`

  - > Connect your machine into the docker swarm
    
      - > \`docker swarm join --token
        > SWMTKN-1-1wnjsb3jyt573yg9a765rua50ytkgcbkuur55m7y2haoc4ze2q-engcpbkxm53gqfociyiz71naa
        > 54.171.68.124:2377\`
        
          - > Note: there will be a different command for the mainnet.
        
          - > If successful, the message will be: \`This node joined a
            > swarm as a worker.\`

  - > Check for success. There should be 3 factom related containers
    > running.
    
      - > $ docker ps
    
      - > CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES
    
      - > a0d79765c855 factominc/metricbeat:m3 "/usr/local/bin/dock…" 8
        > seconds ago Up 7 seconds
        > factomd-services\_metricbeat.0ojxlsrossrngt28on4u2owln.3rqbd9cr1cq68ar5cbxrrnyc5
    
      - > 45a104213a52 factominc/filebeat:m3 "/usr/local/bin/dock…" 9
        > seconds ago Up 8 seconds
        > factomd-services\_filebeat.0ojxlsrossrngt28on4u2owln.kh2n8tcg6255oknuw752kbnpb
    
      - > 648549896ef8 factominc/factom-ssh:m3 "/entrypoint.sh" 33
        > seconds ago Up 32 seconds 22/tcp, 0.0.0.0:22-\>2222/tcp
        > factomd-services\_ssh.0ojxlsrossrngt28on4u2owln.v23t8who4giu3v9j3lanrau67

  - > Pre-populate an existing config file
    
      - > Run \`docker volume create factom\_keys\`
        
          - > Success looks like \`factom\_keys\`
    
      - > As a testnet follower, you can use an example file
        
          - > [<span class="underline">https://raw.githubusercontent.com/FactomProject/communitytestnet/master/factomd.conf.EXAMPLE</span>](https://raw.githubusercontent.com/FactomProject/communitytestnet/master/factomd.conf.EXAMPLE)
        
          - > sudo cp -r \<wherever the example file
            > is\>/factomd.conf.EXAMPLE
            > /var/lib/docker/volumes/factom\_keys/\_data/factomd.conf
    
      - > If you are bringing up a leader, lets brain-swap your existing
        > node into the swarm node. That means starting your node as a
        > follower, but pre-positioning your config file to be ready
        > later.
    
      - > Copy the existing config file to be visible to the docker
        > factomd node
        
          - > \`sudo cp -r \<wherever the config file is\>/factomd.conf
            > /var/lib/docker/volumes/factom\_keys/\_data/factomd.conf\`
    
      - > Use your existing leader config file, but comment out with a
        > semicolon the fields IdentityChainID, LocalServerPrivKey, and
        > LocalServerPublicKey. You can add the line \`IdentityChainID =
        > FA1E000000000000000000000000000000000000000000000000000000000000\`
        > as a placeholder to signify that this node is a follower and
        > that it is properly reading the config file.
    
      - 
  - > Pre-populate an existing database
    
      - > Run \`docker volume create factom\_database\`
    
      - > Note, you cannot copy a database while factomd is running
        > using it.
    
      - > Make sure there is no old database in the docker already.
        
          - > \`sudo ls
            > /var/lib/docker/volumes/factom\_database/\_data\` should
            > be empty
        
          - > \`sudo rm -rf
            > /var/lib/docker/volumes/factom\_database/\_data/\*\`
            > clears out an old database
    
      - > \`sudo cp -r \<wherever the custom-database database
        > is\>/custom-database
        > /var/lib/docker/volumes/factom\_database/\_data/custom-database\`
        
          - > The files in the \_data folder should be the same as are
            > in the \~/.factom/m2 directory hierarchy.
        
          - > The expected folder in \_data is \`custom-database\`
    
      - > Copy the savestate file too if you don’t want to rescan the
        > file
        
          - > \`sudo cp \<wherever the custom-database database
            > is\>/FastBoot\_CUSTOM\_v8.db
            > /var/lib/docker/volumes/factom\_database/\_data\`

  - > Retrieve your node ID from your local machine.
    
      - > Run \`docker info\`
        
          - > Swarm: active
        
          - > NodeID: 0ojxlsrossrngt28on4u2owln
    
      - > The NodeID is used to uniquely identify your machine in the
        > system.

  - > Send this NodeID to the coordinator along with a good human
    > readable name for this machine.

  - 
Docker coordinator will run the add\_node.sh script on the coordination
node linking the NodeID to the team machine name. The linking process
will also connect

Open these incoming ports to the portainer node 54.171.68.124:

  - > 2222 TCP (ssh)

  - > 8090 TCP (control panel)

  - > 8808 TCP (factomd API)

Open these ports to the internet:

  - > 8110 TCP (P2P Testnet)
    
      - > For mainnet use 8108 TCP (P2P Mainnet)

<!-- end list -->

  - > To remove your node from the swarm to restart the procedure
    
      - > \`docker swarm leave\`
        
          - > The expected result would be \`Node left the swarm.\`
    
      - > \`docker ps\` should show there is no more factom docker
        > images running.
    
      - > \`docker ps -a\` will show that they are gone and not just
        > stopped.

  - > Delete the old database if appropriate
    
      - > \`sudo ls /var/lib/docker/volumes/factom\_database/\_data\`
        > should be empty
    
      - > \`sudo rm -r
        > /var/lib/docker/volumes/factom\_database/\_data/\*\` clears
        > out an old database

  - > Delete the config file if appropriate
    
      - > \`sudo ls /var/lib/docker/volumes/factom\_keys/\_data\` should
        > be empty
    
      - > \`sudo rm -r /var/lib/docker/volumes/factom\_keys/\_data/\*\`
        > clears out an old database
