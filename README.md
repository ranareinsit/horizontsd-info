# horizontsd-info

<p align="center">

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)
![Code Coverage](coverage.svg)

</p>

# Запуск на своей машине

#### Установка зависимостей
```bash
apk update 
apk upgrade
apk add --no-cache libc6-compat
npm install -g corepack
npm -v
corepack enable
corepack install --global yarn@4.7.0
```

Активация окружения
```bash
cd horizontsd-info
yarn install
```

Запуск на своей машине
```bash
yarn dev
yarn build
yarn start
yarn lint
```

# Запуск контейнера локально

### Строим контейнер
```bash
sudo docker build --pull --rm -f Dockerfile -t horizontsdinfo:latest . --progress=plain
```

Узнаем его ID
```bash
sudo docker images
```

```bash
sudo docker run -d -p 3000:3000 <IMAGE ID>
```

# Запуск контейнера публично

### Строим контейнер
```bash
sudo docker build -t horizon_info .
```
Узнаем его IMAGE ID
```bash
sudo docker images
```

```bash
docker run -d -p 3000:3000 <IMAGE ID>
```

```bash
docker run -d -p 80:3000 <IMAGE ID>
```

```bash
docker run -d -p 3000:80 <IMAGE ID>
```
