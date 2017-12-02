## App Design

### p2p, accounts, keys and nodes
- Refer to p2p.md

### App Shell
- We are using https://gopkg.in/urfave/cli.v1 for the CLI app shell

### Runtime Metrics
- We are using https://github.com/rcrowley/go-metrics for system metrics

### Local DB
- We are using goleveldb for a key-value db

### Dependencies
- We are using govendor for versioned deps
- We add all vendored libs to git
- Always add a dep using govendor
- For a major dep we use wrappers. See logging.
- Danger: Do not add a dep from github directly using `go get` without using vendoring.

### Debugging

#### GoLand IDEA interactive debugging
- Should be fully working - create an IDEA config to run main in the proj root source dir

#### Other ways to debug

### Logging
- We are using [go-logging](https://github.com/op/go-logging)
- Use /log/logger wrapper funcs for app-level logging
- You may add custom loggers (per package, to a file, etc...)

### Config
- We are using TOML files for config file and cli.v1 flags to modify any configurable param via the CLI.

### Interactive Console
- TBD - Javascript console ???? do more research