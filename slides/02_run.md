# Run K9s

Running k9s with specific context

```sh
k9s --context my-cluster
```

Running k9s with specific namespace

```sh
k9s -n my-namespace
```

Running k9s with view on a specific resource

```sh
k9s -c deploy
```

---

**NOTE:** When opening K9s without any argument, it will open the context that is currently active in your shell.
