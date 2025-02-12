# Docker config mongodb atlas

## Här hittar du config filer för att sätta upp Docker med MongoDB Atlas
Läs igenom instruktionen noga för jag har skrivit vad ni behöver ändra i tex MongoDB Atlas connection strängen.

### Dockerfile
Skapa en Dockerfile i root, alltså högerklicka på huvudmappen högst upp och och välj new => file
Döp filen till **Dockerfile** och inget annat.
Kopiera innehållet ifrån **Dockerfile** i det här repot och klistra in

### docker-compose.yml
Skapa en docker-compose.yml i root, alltså högerklicka på huvudmappen högst upp och och välj new => file
Döp filen till **docker-compose.yml** och inget annat.

Ni skriver ert projekt namen på raden för **container_name**
```yaml
container_name: your-project-name
    ports:
      - "8081:8080"
```
**ports** har vi satt till 8081:8080 för att ni ska kunna köra Docker instansen detached.
Det innebär att ni startar docker sen startar ni Spring boot precis som vanligt inne i IntelliJ. Spring kör på port 8080 och Docker instansen på 8081

### application.yml
Ni skapa en ny fil i mappen resources, där ni har application.properties, och döper den till **application.yml**
Ni kan kopiera innehållet från det här repot och klistra in.

