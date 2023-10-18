# [Basaran](https://github.com/hyperonym/basaran/) demo app for Fly.io

First deploy with:
```
fly apps create basaran-demo
fly deploy --vm-gpu-kind a100-pcie-40gb --volume-initial-size 100
```

From there for following deploys use:
```
fly deploy
```

Once deployed, go to https://basaran-demo.fly.dev/
