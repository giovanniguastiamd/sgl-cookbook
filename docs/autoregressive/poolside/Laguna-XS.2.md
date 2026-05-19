

## AMD MI355X

### Model Deployment

```bash
sglang serve \
  --model-path poolside/Laguna-XS.2 \
  --tp 8 \
  --reasoning-parser poolside_v1 \
  --tool-call-parser poolside_v1 \
  --host 0.0.0.0 \
  --port 30000
```

## AMD MI300X

### Model Deployment

```bash
sglang serve \
  --model-path poolside/Laguna-XS.2 \
  --tp 8 \
  --reasoning-parser poolside_v1 \
  --tool-call-parser poolside_v1 \
  --host 0.0.0.0 \
  --port 30000
```
