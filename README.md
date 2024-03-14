# TacticalRMM_Agent_Build_Notes
Memo : to build Tactical RMM agents

# Prerequisit
- Clone rmmagent repo
- Install go

# Build linux
- Build linux agent `env CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -ldflags "-s -w"`.
- Copy the rmmagent binary on your target.
- On your RMM UI do Agent > Install agent >Windows > Server or Workstation > Manual > Show manual installation instruction > Copy all the parameters after `tacticalrmm.exe"`.
- Install the agent with the command `sudo ./rmmagent PASTEHERE` (example: `sudo ./rmmagent -m install --api https://xxxx --client-id 1 --site-id 1 --agent-type server --auth XXXXXXXX`)
