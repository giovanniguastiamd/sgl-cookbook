

## AMD MI355X

### Model Deployment

```bash
SGLANG_ENABLE_SPEC_V2=1 sglang serve \
  --model-path zai-org/GLM-5.1-FP8 \
  --tp 8 \
  --trust-remote-code \
  --nsa-prefill-backend tilelang \
  --nsa-decode-backend tilelang \
  --chunked-prefill-size 131072 \
  --watchdog-timeout 1200 \
  --reasoning-parser glm45 \
  --tool-call-parser glm47 \
  --speculative-algorithm EAGLE \
  --speculative-num-steps 3 \
  --speculative-eagle-topk 1 \
  --speculative-num-draft-tokens 4 \
  --mem-fraction-static 0.9
```

#
