# dsh-linux-bundle

A prebuilt Linux x64 copy of the DeepSeek Harness (`dsh`, npm `@deepseek-ai/dsh`) for machines where the npm registry is blocked but GitHub is reachable.

- Upstream: https://github.com/deepseek-ai/deepseek-harness (MIT, see `LICENSE` and `THIRD_PARTY_NOTICES.md`). Not affiliated with DeepSeek.
- Built: `npm install -g --prefix /out @deepseek-ai/dsh@0.2.2-rc.5` inside `docker node:24` (Node v24.22.3), 2026-11-24.
- Needs Node >= 24.9 on PATH.

```bash
curl -L -o dsh.tgz https://github.com/jluo41/dsh-linux-bundle/releases/download/v0.2.2-rc.5/dsh-0.2.2-rc.5-linux-x64.tgz
mkdir -p ~/dsh && tar xzf dsh.tgz -C ~/dsh
export PATH=~/dsh/bin:$PATH && dsh --version
```
