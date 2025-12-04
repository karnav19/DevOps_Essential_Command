# GitHub Actions Runner (Self-hosted) — Step-by-step

## Download runner
```bash
mkdir actions-runner && cd actions-runner
curl -o actions.tar.gz -L https://github.com/actions/runner/releases/latest/download/actions-runner-linux-x64.tar.gz
tar xzf actions.tar.gz
```

## Configure & run
Follow GitHub repo Settings → Actions → Runners → New self-hosted runner to get the registration token, then:
```bash
./config.sh --url https://github.com/<owner>/<repo> --token <TOKEN>
./run.sh
```

## Tips
- Run as systemd service for production.
