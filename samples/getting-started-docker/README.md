# Getting Started with Docker

→ [learn.hashicorp.com](https://learn.hashicorp.com/collections/packer/docker-get-started)

## Commands

```bash
# initializes the Packer configuration
packer init .

# formats the template
packer fmt .

# validates the template
packer validate .

# builds the image (review the output for the expected messages)
packer build docker-ubuntu.pkr.hcl

# looks at the generated image
docker images

# launches the newly created Docker image and starts an interactive shell
docker run -it <IMAGE_ID>

# makes sure the file example.txt has been created
cat example.txt

# exists the shell inside the container
exit

# builds the image with a variable file (review the output for the expected messages)
packer build --var-file=example.pkrvars.hcl docker-ubuntu.pkr.hcl

# builds the image with a variable from the command line (review the output for the expected messages)
packer build --var docker_image=ubuntu:groovy .

# reviews created containers and delete them
docker ps --all
docker rm <CONTAINER_ID>

# deletes the images
docker rmi <IMAGE_ID>
```
