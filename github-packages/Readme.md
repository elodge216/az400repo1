export GH_USERNAME='elodge216'
export GH_TOKEN=''
export GH_IMAGE_NAME='hello-world'
export GH_VER='1.0.0'
echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag $GH_IMAGE_NAME:latest ghcr.io/elodge216/$GH_IMAGE_NAME:$GH_VER

docker push ghcr.io/elodge216/hello-world:1.0.0