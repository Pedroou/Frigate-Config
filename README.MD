## Commands for Running Frigate

### Build the Container

```bash
cd frigate-dev/
docker buildx bake -f docker/tensorrt/trt.hcl tensorrt
```

### Run the Built Container

```bash
cd frigate/
docker compose up
```

### Enter the Container

```bash
docker exec -it frigate bash
```

### Check if the Custom Frigate Version is Being Used

```bash
cat /PEDROOU_MARKER.txt
# Should output: PEDROOU CUSTOM BUILD
```

---

## How to Update the Frontend in Frigate

### Run the Frontend

```bash
npm run dev
```

### Build the Frontend

```bash
cd /path/to/frigate-dev/web
npm ci          # Only needed the first time or when dependencies change
npm run build
```

*Then build the container again for the changed frontend to be applied.*
