```sh
$ k get po -o yaml | less

spec:
  initContainers:
  - image: busybox
    name: warmup-1
    command: ["sh", "-c", "sleep", "1200"]
```