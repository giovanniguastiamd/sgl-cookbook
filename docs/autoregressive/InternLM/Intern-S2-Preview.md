

```markdown
## AMD MI355X

### Docker Setup

```bash
docker run -d \
  --device=/dev/kfd --device=/dev/dri \
  --group-add video --cap-add=SYS_PTRACE \
  --security-opt seccomp=unconfined \
  --shm-size=32g --ipc=host --network=host \
  lmsysorg/sglang-rocm:v0.5.12-rocm720-mi30x-20260517 bash
```

### Model Deployment

```bash
python \
  -m sglang.launch_server \
  --model InternLM/Intern-S2-Preview \
  --tp 8 \
  --attention-backend triton \
  --trust-remote-code \
  --context-length 8192 \
  --mem-fraction-static 0.85 \
  --host 0.0.0.0 \
  --port 30000
```

#
