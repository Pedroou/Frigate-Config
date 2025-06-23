### ---- Commands for running Frigate ----

# -- Command for building the container:
cd frigate-dev/
docker buildx bake -f docker/tensorrt/trt.hcl tensorrt

# -- Command for running the built container:
cd frigate/
docker compose up

# -- Command for entering the container:
docker exec -it frigate bash

# -- Command for checking if the custom Frigate version is being used:
cat /PEDROOU_MARKER.txt		# Should output: PEDROOU CUSTOM BUILD


### ---- How to update the frontend in Frigate ----

# -- Command for running the frontend:
npm run dev

# -- Command for building the frontend:
cd /path/to/frigate-dev/web
npm ci         # Only needed the first time or when dependencies change
npm run build

# -- Then build the container for the changed frontend to be applied.
