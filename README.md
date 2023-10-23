# docker-geospatial-tools

* Get into docker directory and run the Dockerfile :

        docker build -t suite .
* A docker-image named strabon is available either locally (previously built), or in DockerHub. Use the docker-image (terminal of your machine): 

        docker run --name suite-container -p 9999:8080 -v /<some_local_dir>:/inout suite
* Now the docker-container strabon-container should be running. Use (the command line of) the container (different terminal on your machine): 

        docker exec -it suite-container /bin/bash
* Finally, start tomcat on the docker terminal :
        
        ./usr/local/bin/conf.sh

Now Strabon and Sextant is available in your machine's port 9999 :

http://localhost:9999/Strabon

http://localhost:9999/Sextant
