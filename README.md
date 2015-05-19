# bug
Demonstrates Kubernetes Issue 8478

0. I've only demonstrated this on GCE, so do this on GCE.
1. Make sure you have a persistent disk named 'workspace' (or change the files to say something else)
2. Bring up a cluster with 3 minions, then...

```bash
  kubectl create master.json
  kubectl create slaves.json
```

* master will schedule
* two slaves will schedule to the two machines that master is not on
* one slave will remain unassigned
