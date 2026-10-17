# Pooled local GPU guide

NEXUS integrates [Pooled](https://github.com/Nehanth/pooled), an MIT-licensed layer-distributed inference runtime. Inference uses Dawn/WebGPU; connected devices exchange intermediate model data through WebRTC. The host coordinates generation and the local bridge exposes a compatible chat endpoint to NEXUS.

## Run on this PC

1. Open Store → Local models → Pooled.
2. Keep **This computer · private local room** selected.
3. Select a model, context capacity and an absolute model folder with enough free space.
4. Choose **Download & start**. The first start downloads weights and verifies checksums. Wait for **Online**.
5. Choose **Use in chat / Mix**, then select the Pooled connection in Chat. For Mix, select suitable roles and include Pooled among your execution providers.
6. Choose **Stop & free GPU** when finished. Restart the runtime after reopening NEXUS; it does not silently load a model at startup.

| Model option | Approximate download | Guidance |
| --- | --- | --- |
| Qwen3 0.6B Q8 | 0.64 GB | Smoke tests; 2K context, weak coding/tool reliability. |
| Qwen3 1.7B Q8 | 1.84 GB | Basic local tasks; about 4 GB room memory at 8K context. |
| Qwen3 4B Q8 | 4.3 GB | More memory required; this integration limits context to 2K. |
| Qwen3.8 27B Q4 | 16.1 GB | Requires substantial aggregate GPU memory. |
| Qwen3.6 35B MoE Q4 | 20.84 GB | Requires substantial aggregate GPU memory. |

These are Pooled catalog options, not a promise that every model fits your computer. Windows, other applications and context buffers also consume memory. Supported models are text-only in this integration.

## Trusted device rooms

**Host a room** creates a shareable private invite; other devices need compatible Pooled software. **Connect an existing room** accepts its complete private invite and attaches a local bridge. The latter does not itself contribute this PC's GPU as a worker. Use Pooled's upstream join flow for contributing another GPU.

Only share with trusted devices: room participants process model data associated with prompts and tool results. Shared rooms use public signaling. Even local setup may contact upstream relay/STUN configuration; this release is not advertised as fully network-isolated. Multi-device operation was not verified on multiple physical machines.

## Troubleshooting

- **Port 8088 busy:** stop the existing Pooled bridge before starting another.
- **GPU allocation failure:** close other GPU workloads, reduce context or choose a smaller model.
- **Download interrupted:** keep the same model folder and retry; Pooled can resume supported downloads.
- **Online but poor answers:** connection success is separate from model quality. Small models are unreliable for complex autonomous coding.
- **No chat provider after start:** select **Use in chat / Mix** after the model reaches Online.

The 300 specialist roles are instruction profiles. Pooled serializes model inference; selecting 300 roles does not launch 300 model copies. Review usage, changed files and actual tool/check evidence.

[Pooled upstream documentation](https://github.com/Nehanth/pooled/blob/main/cli/README.md) · [Release notes](RELEASE-0.6.19.md)
