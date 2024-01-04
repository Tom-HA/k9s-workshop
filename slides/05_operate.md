# Operate on resources

In K9s you can perform actions on resources like, enter a pod shell, delete a resource, scale a resource, etc.  
**NOTE:** You can select multiple resources by pressing `space` on them.

## Get logs

You can use K9s to get logs for deployments or pod by hovering over the desired resource and press `l`  

## Delete resources

You can delete pods by hovering over a pod, press `ctrl-d` and confirm.  
To delete multiple pods at once, press `space` on multiple pods, then press`ctrl-d` and confirm.

## Scale resources

You can scale deployments by hovering over them and press `s`, then enter the desired number of replicas

## Enter pod shell

You can enter a pod shell by hovering over a pod and press `s`

## Get secret content

To get a secret value, search for secrets in k9s by running

```k9s
:secret
```

Hover over your desired secret and press `x`, this will decode your secret's value which is encoded originally in base64.  

## Port-forward

You can initialize port forwarding in K9s to connect to a `pod` or a `service`.  
For example, in K9s, hover over a service you would like to initialize a connection with, and press `<shift-f>`

```k9s
:svc
<shift-f>
```

You will be prompted with the port-forward settings. Here you can configure the container name and port number of the desired pod, and the port in you local machine.  
Once you confirmed the settings you should be able to access your `service` by going to `localhost` at the configured port.  

To check existing `port-forwards`, in K9s you can execute

```k9s
portforward
```

Or

```k9s
pf
```

To terminate a port-forwarding session, hover over the desired `port-forward`, press `<ctrl-d>` and confirm.
