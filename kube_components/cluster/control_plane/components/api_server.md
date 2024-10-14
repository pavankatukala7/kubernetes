## API Server

- Exposes the Kubernetes API, which is used by other components and users to interact with the cluster.
- The Kubernetes API server is the main entry point for all interactions with the cluster. Users and components communicate with it using HTTP requests to perform CRUD (Create, Read, Update, Delete) operations on various resources.

**Examples of API Usage**:
- `kubectl get nodes`: Makes a call to the Kubernetes API server (GET /api/v1/nodes).
- `kubectl create deployment my-app --image=my-image`: Corresponds to a POST request to the API server (POST /apis/apps/v1/namespaces/default/deployments).
- `kubectl edit deployment my-app`: Sends a PUT request to the API server (PUT /apis/apps/v1/namespaces/default/deployments/my-app).
- `kubectl delete pod my-pod`: Deletes a resource like a pod (DELETE /api/v1/namespaces/default/pods/my-pod).
- `kubectl get pods --watch`: Sets up a long-lived GET request to watch for changes (GET /api/v1/namespaces/default/pods?watch=true).


- [etcd](./etcd.md): Information about etcd and its role in Kubernetes.
- [Controller Manager](./controller_manager.md): Overview of the kube-controller-manager and its controllers.
