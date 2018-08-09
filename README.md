Hit the bug
---- 

```COMPOSE_HTTP_TIMEOUT=7200 docker-compose -f docker-compose-bug.yml up --no-recreate```

This will create `.gradle` folder in the current folder and will be shared with both containers `/root/.gradle`


Avoid the bug
---- 


```COMPOSE_HTTP_TIMEOUT=7200 docker-compose -f docker-compose-fixed.yml up  --no-recreate```

This will create `.gradle-files` folder on the host machine, in the current folder and will be shared with both containers for `/root/.gradle/caches/modules-2/files-2.1/`

