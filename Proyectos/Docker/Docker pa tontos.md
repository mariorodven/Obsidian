## Programa de prueba en Docker

1. Clona el repositorio
```bash
$ git clone https://github.com/docker/getting-started-app.git
```
Deberíamos ver algo así:
```
├── getting-started-app/
│ ├── package.json
│ ├── README.md
│ ├── spec/
│ ├── src/
│ └── yarn.lock
```
2. Accedemos al directorio y creamos el Dockerfile
```bash
cd getting-started-app
touch Dockerfile
code .
```
3. Usando el vs code por ejemplo escribiremos lo siguiente en el Dockerfile:
```dockerfile
# syntax=docker/dockerfile:1

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
```
4. Generamos la imagen ejecutando:
```bash
docker build -t getting-started .
```
Este comando tiene varias partes. Te habrás dado cuenta que al ejecutar esto se han descargado muchas cosas, entre ellas el alpine Linux que hemos especificado antes, pues a menos que tengamos la imagen previamente instalada, la tendrá que descargar. Además, con el ```-t``` le damos un nombre a la imagen que estamos compilando, y con el ```.``` le decimos que busque el Dockerfile dentro del directorio actual. 