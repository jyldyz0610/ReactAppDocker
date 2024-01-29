# ReactAppDocker


1. React-App erstellen
npx create-react-app react-docker-tutorial

2.Dockerfile erstellen innerhalb react-docker-tutorial

3.docker image build -t <image_name>:<tag> <path>  also  docker image build -t react-tutorial-image:latest .

4.docker run -dp <Host-Port>:<Container-Port> --name <Container-Name> <Image-Name>:<Tag>

5. docker image ls
6. docker run -dp 8000:3000 --name react-tutorial-container react-tutorial-image:latest



Mit Dockerhub:

1. Create Repository.
2. docker login
3. docker image tag react-tutorial-image <username>/react-tutorial-image
4. docker push jyldyz0610/react-tutorial-image
5.  docker image build -t react-tutorial-image:upgrade .
6. docker image tag react-tutorial-image:upgrade <username>/react-tutorial-image:upgrade
7.docker push jyldyz0610/react-tutorial-image:upgrade
8. docker run -dp 8000:3000 --name react-tutorial-container react-tutorial-image:latest
9.docker stop <name>