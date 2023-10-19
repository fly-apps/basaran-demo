# [Basaran](https://github.com/hyperonym/basaran/) demo app for Fly.io

First deploy with:
```
fly apps create basaran-demo
fly deploy --vm-gpu-kind a100-pcie-40gb --volume-initial-size 100 --wait-timeout 600
```

From there for following deploys use:
```
fly deploy
```

Once deployed, go to https://basaran-demo.fly.dev/


## HuggingFace token

Some models requires a huggingface token to access, create one
at https://huggingface.co/settings/tokens and set it as a
secret with `fly secrets set HUGGINGFACE_TOKEN=<token>`

Once set, change the MODEL envvar in fly.toml.

i.e.:
    MODEL="huggyllama/llama-7b"
