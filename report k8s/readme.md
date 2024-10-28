

# 1. Create a Pod Named Redis with the Redis Image

To create the pod, use a `YAML` file with the following command:

```bash
kubectl apply -f q1/redis-pod.yml
```

## 1. Verify Pod Creation

Once the command above is executed, check the pod’s status with:

```bash
kubectl get pod
```

![Image showing the `kubectl get pod` command output](image.png)

## 2. Accessing Redis

To access Redis, you can use a Kubernetes Service (Cluster Access). However, if this feels complex, **Port Forwarding (Local Access)** is a simpler alternative that allows direct local access to Redis.

Forward the Redis port to your local machine with:

```bash
kubectl port-forward pod/redis 6379:6379
```

![Image showing the `kubectl port-forward` command output](image-1.png)

## 3. Connecting to Redis

After port-forwarding, connect to Redis locally with:

![Example of accessing Redis](image-2.png)

> [!IMPORTANT]  
>You must install `redis-cli` to access Redis. If you haven’t installed it yet, [follow the instructions here](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/).

---