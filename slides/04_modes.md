# Changing modes

Like in VI, you can use `:` and `/` to change modes.  

In K9s, you can view resources using `:`. For example, to view `deployments`

```k9s
:deploy
```

This is equivalent to

```sh
kubectl get deploy
```

Whenever you wish to `get` a resource, you should use `:` followed by the desired resource name.  

You can also use `:` to switch context and namespace:

* View context list

  ```k9s
  :ctx
  ```

* Quickly enter a new context

  ```k9s
  :ctx my-cluster
  ```

* View namespace list

  ```k9s
  :ns
  ```

* Get resource in namespace

  ```k9s
  :deploy my-namespace
  ```

* Get resource in a different context

  ```k9s
  :deploy @my-cluster
  ```

To filter resources by name, use `/` to enter filter mode, then, write the desired filter and press `enter`.  
Here are a few examples for filters:

* Filter deployments that match the name `my-deployment`

  ```k9s
  /my-deployment
  ```

* Filter deployments that **do not** match the name `my-deployment`

  ```k9s
  /!my-deployment
  ```

## Combine modes

You can combine the `:` and `/` modes together, for example

* Get `deployments`, in `my-cluster` context, in the `my-namespace` namespace, filtered by `my-deployment`

  ```k9s
  :deploy @my-cluster my-namespace /my-deployment
  ```
