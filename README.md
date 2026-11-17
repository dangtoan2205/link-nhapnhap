```
New-Item -ItemType Directory -Force C:\docker-offline

docker save -o C:\docker-offline\oxi-images.tar oxi-main-app:latest nginx:stable-alpine
```

