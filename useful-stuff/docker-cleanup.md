- **Remove current project containers, network, and anonymous volumes**

```
docker compose down --remove-orphans -v
```

- **Check current Docker disk usage**

``` 
docker system df
```

- **Build Cache Cleanup**

```  
docker builder prune
```

- **Force remove all unused build cache**

```  
docker builder prune -af
```

- **Remove stopped containers**

```  
docker container prune -f
```

- **Remove unused networks**

```  
docker network prune -f
```

- **Remove dangling images only**

```  
docker image prune -f
```

- **Remove all unused images, not just dangling**

```  
docker image prune -af
```

- **To Check docker networks**

```  
docker network ls
```

- **To stop a network** 

```
docker stop <network-name>
```
- **Remove everything**

```
docker system prune -a --volumes
```
