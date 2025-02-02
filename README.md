**Git Clone:**
```
https://github.com/cinetube/docker-filegator-2
```

**Build Docker image:**

```
docker build -t cinetube/filegator:latest .
```

**Docker Compose (AMD64):**

```
version: '3.7'

services:
  filerun:
    image: cinetube/filegator:latest
    container_name: filegator
    ports:
      - 8085:80
    environment:
      PUID: 1000
      PGID: 1000
      TZ: Asia/Dhaka
    volumes:
      - /mnt/filegator/data:/data
      - /mnt/filegator/config:/config
    restart: always
```

**Docker Compose (ARM):**

```
version: '3.7'

services:
  filerun:
    image: cinetube/filegator:arm
    container_name: filegator
    ports:
      - 8085:80
    environment:
      PUID: 1000
      PGID: 1000
      TZ: Asia/Dhaka
    volumes:
      - /mnt/filegator/data:/data
      - /mnt/filegator/config:/config
    restart: always    
```    

Login as admin with default credentials admin/admin123

```
version: '3.7'

services:
  filerun:
    image: cinetube/filegator:arm
    container_name: filegator
    ports:
      - 8085:80
    environment:
      PUID: 1000
      PGID: 1000
      TZ: Asia/Dhaka
    volumes:
      - /mnt/downloads:/data
      - /mnt/filegator/config:/config
    restart: always    
```
