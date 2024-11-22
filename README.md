## Startup Instructions


1) Download Herd from [here](https://herd.laravel.com/)  
2) allow it to modify the path on install(to have php in your path)
3) move this project to the Herd directory  `cd ~/Herd
3.1) before composer install you need [grpc](https://github.com/grpc/grpc/tree/master/src/php) installed, needed by new versions of google firestore!
3.2) move the dll(on windows) to the Herd folder C:\Users\[your path name]\.config\herd\bin\php83
3.3) in the php.ini file register the dll: 
```php
[Herd]
extension=".\php_grpc.dll"
```
3.4 restart herd(from the show hidden icons tray)
4) run `composer install`
5) run npm install && npm run build 
6) run `php artisan migrate:fresh`
7) npm run dev

## Environment Variables

In the env file change the firestore credentials path:

FIREBASE_CREDENTIALS="C:/Users/baned/Downloads/BMW/electionapp-512e2-firebase-adminsdk-1qd20-487de6af9f.json"
GOOGLE_CLOUD_PROJECT="C:/Users/baned/Downloads/BMW/electionapp-512e2-firebase-adminsdk-1qd20-487de6af9f.json"