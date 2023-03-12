    ./mvnw package -Pnative  -Dquarkus.native.container-build=true -Dquarkus.native.builder-image=graalvm
    
    docker build -f src/main/docker/Dockerfile.native -t quarkus/simple-app . 
    
    docker run --rm -p 8080:8080 quarkus/simple-app
