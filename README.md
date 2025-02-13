# wavenure-finance-app

Welcome to wavenure-finance-app!

It contains two submodules, one for the backend and one for the fontend:

- **mobile**: it has been developed in Expo and is compatible with both iOS and Android platforms. Below you will find the necessary information to set up the development environment, run the project, and test the code.

- **backed**: It as a RestAPI server for the mobile app; it has been developed with NodeJS + Express + Posgress + Prisma

## Prerequisites

Before getting started, make sure you have the following software installed:

Mobile:

1. **Asfd**: To manage the versions of Node.js, Java, and Ruby, you need to have asdf installed. Refer to the official documentation for installation: [asdf](https://asdf-vm.com/).

Backend:

1. **Docker**: To run Postgresql locally, install Docker following the official guide: [Docker Installation](https://docs.docker.com/get-docker/).

## Init repository submodule

The main Repository is composed of two submodules: **backend** and **mobile**. To download the code you need to run the following commands:

```
$ git clone https://github.com/lucaCicc/wavenure-finance-app.git
```

```
$ cd wavenure-finance-app
```

```
$ git submodule update --init --recursive
```

# BACKEND

You can launch the backed and DB with a docker container. Run the following command on terminal:

```
$ cd backend
```

```
$ git checkout develop
```

```
$ docker compose up
```

**TEST USER**: In migrations I added a test user; with this you can log in with the mobile app

- **user**: test.test@gmail.com
- **psw**: 123456

If you want to run the backend without docker you have to:

1. create the .env file in the root of the project and copy the contents you find in the env.default file

```
$ yarn install
```

```
$ yarn start
```

# FRONTEND

To launch tha mobile apllication:

```
$ cd mobile
```

```
$ git checkout develop
```

1. Install the specified versions of Node.js, Java and Ruby found in the file .tool-version (optional you can also use the versions you have on your PC but but problems may occur!)

```
$ asdf install
```

2. Install project dependencies

```
$ yarn install
```

```
$ bundle install
```

```
$ cd ios
$ bundle exec pod install
```

2. Install project dependencies

Creates an **.env** file and enter the following key

```
EXPO_PUBLIC_API_URL=http://localhost:3000/api
```

If you use a physical device you must enter the local IP of the PC.

```
$ ipconfig getifaddr en0
```

```
EXPO_PUBLIC_API_URL=http://{local_ip}:3000/api
```

## Application Launch

To launch the application on **Android**:

Create **local.properties** file under **android** folder.
Paste these lines inside:

```
RELEASE_KEY_ALIAS=test
RELEASE_KEY_PASSWORD=test
RELEASE_STORE_FILE=test
RELEASE_STORE_PASSWORD=test
```

```
$ yarn android
```

To launch the application on **Ios**:

```
$ yarn ios

```

```

```
