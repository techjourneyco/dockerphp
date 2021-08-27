These Docker files allows you to run a PHP basic project.

## Extra
The container has XDebug and MYSQL dependencies loaded.

## Usage

You can build the container using this command:

First time
```bash
docker-compose up -d --build
```

If you shutdown your computer or you down the container and if you don't make any changes to the Dockerfile or docker-compose.yml settings, you can run the container again using this command:
```bash
docker-compose up -d
```

## Usage
When the container is run, you can use Visual Studio Code(https://code.visualstudio.com/) and Remote - Containers extension (https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) to work with this.

Remember that this github repository is only for testing PHP scripts or PHP applications. This repository isn't recommended to production enviroments.

If you like test a PHP script, only you need to create a PHP file in the root of the container or if you wish, you could create a directory and save your PHP scripts.

Open yor prefered browser and open the following URL:

http://127.0.0.1/[yourscript.php]

Or 

http://127.0.0.1/[yourdirectory]/[yourscript.php]


## Debugging application

The docker-compose file has a xDebug configuration to allow you to debug your PHP application.

I did the xDebug configuration using Visual Studio Code(https://code.visualstudio.com/) and PHP Debug extension(https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug)