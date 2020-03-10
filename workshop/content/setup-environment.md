To view the OpenShift web console, click on the **Console** tab in the workshop dashboard. You should find that OpenShift web console is already connected to the Kubernetes cluster and it is displaying an overview for the `%session_namespace%` namespace.

So that we have a real application to work with and investigate, first run in the terminal the command:

```execute
oc apply -f database
```

This will deploy a PostrgreSQL database.

Did you type the command in yourself? If you did, click on the command instead and you will find that it is executed for you. You can click on any command which has the <span class="fas fa-running"></span> icon shown to the right of it, and it will be copied to the interactive terminal and run. If you would rather make a copy of the command so you can paste it to another window, hold down the shift key when you click on the command.

To monitor the deployment of the database, run:

```execute
oc rollout status deployment/blog-db
```

When the deployment of the database has completed, run:

```execute
oc apply -f frontend
```

This will deploy a blog application, with it being connected up to the database for storage.

To monitor the deployment of the blog, run:

```execute
oc rollout status deployment/blog
```

Now that we have deployed some workloads, let's explore the OpenShift web console. Jump back to the view the OpenShift web console by clicking on the **Console** tab in the workshop dashboard.
