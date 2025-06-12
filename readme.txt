command for building the container:
cd frigate-dev/
docker buildx bake -f docker/tensorrt/trt.hcl tensorrt

command for running the built container:
cd frigate/
docker compose up

command for entering the container:
docker exec -it frigate bash

command for checking if the custom frigate version is being used:
cat /PEDROOU_MARKER.txt
# Should output: PEDROOU CUSTOM BUILD

# If you see the above, you are running your own custom image.
