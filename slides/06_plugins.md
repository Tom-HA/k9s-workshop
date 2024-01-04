# Add plugins

To add plugins, execute `k9s info` to get the plugin directory, for example

```sh
k9s info

...
Plugins:           /Users/my-user/Library/Application Support/k9s/plugins.yaml
```

Now add to this path your desired plugin, you can check under [plugins](../plugins/) directory an example `plugins.yaml` file with the `stern` plugin.  
This plugin will allow you to get logs from pods that match the name in the K9s filter.  

For example, in k9s when you filter `pods` by the name `my-pod` and then press `<ctrl-l>`, `stern` will fetch the logs from pods that contain the name `my-pod`

```k9s
:pod
/my-pod
<ctrl-l>
```

**NOTE:** Make sure you have `stern` installed! You can find `stern` installation documentation [here](https://github.com/stern/stern?tab=readme-ov-file#installation).

---

For more information about K9s plugins, check their documentation [here](https://github.com/derailed/k9s?tab=readme-ov-file#plugins).