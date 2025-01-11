To start the application:

1. Run each Dockerfile and publish the image to your DockerHub or just use the pre-built images: https://hub.docker.com/u/krisssssssss (already in the source code)
                          
2. Set up cluster infrastructure:
    Create a cluster
    - eksctl create cluster --name <name-of-cluster> --region <region> --node-type t3.medium  --nodes 3  --nodes-min 3 --nodes-max 6 --managed

    Apply the manifests
    - kubectl apply -f frontend.yaml
    - kubectl apply -f backend.yaml
    - kubectl apply -f postgres.yaml

    Get the DNS
    - kubectl get svc backend-service
    - paste the external IP in the browser

Enjoy! :)




