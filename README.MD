## Frigate Commands

### GPU Version (TensorRT)

#### Build the TensorRT Image
```bash
cd frigate-dev/
make local-trt
```

#### Run Frigate with GPU
```bash
cd frigate/
docker compose up
```

#### To enter the TensorRT Container
```bash
docker exec -it frigate bash
```

---

### CPU Version (Proxmox)

#### Build the CPU Image
```bash
cd frigate-dev/
make local
```

#### Run Frigate with CPU
```bash
cd frigate/
docker compose up
```

---

### Verify Custom Build
#### Check if the Custom Version in Use
```bash
docker exec -it frigate cat /PEDROOU_MARKER.txt
# Should output: PEDROOU CUSTOM BUILD
```

---

## Frontend Development

### Run the Frontend Locally
```bash
cd /path/to/frigate-dev/web
npm run dev
```

### Build the Frontend
```bash
cd /path/to/frigate-dev/web
npm ci          # Only needed the first time or when dependencies change
npm run build
```

---

## Notes
- TensorRT builds require the `runtime: nvidia` setting in `docker-compose.yml`.
- For CPU builds, comment out `runtime: nvidia` in the `docker-compose.yml` file.

---

## Command to open current path in Windows Explorer

```bash
explorer.exe .
```
