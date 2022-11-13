# Login ke Heroku CLI

Sebelum masuk ke tahap ini pastikan aplikasi berada dalam direktori & `heroku CLI` sudah diinstall.

* Masuk ke terminal / command prompt pada folder aplikasi, kemudian jalankan perintah :

`$ heroku login`

Heroku akan mengarahkan kita untuk login via browser.

![1668156874532](image/heroku/1668156874532.png)Setelah berhasil, pada terminal akan menampilkan email kita, seperti output pada terminal berikut:

```bash
heroku: Press any key to open up the browser to login or q to exit:
Opening browser to https://cli-auth.heroku.com/auth/cli/browser/c57590ec-7f1b-45d5-9a2e-16aa9f2c8680?requestor=SFMyNTY.g2gDbQAAAA8xMDMuMTQ0LjE3NS4yMzBuBgAQPdZlhAFiAAFRgA.vICSJphBLdfnNdXAi8VjVQBmmQ5OJk9Ka-gwDvPJePM
Logging in... done
Logged in as aninomus.ani@gmail.com
```

*heroku cli login berhasil ☝🏻*

## Mendaftarkan Aplikasi di Heroku

Aplikasi yang telah kita buat, perlu didaftarkan terlebih dahulu dengan menjalankan perintah :

```bash
heroku create nama-aplikasi-kita
```

Ketika pendaftaran aplikasi berhasil, maka kita sudah bisa mengakses aplikasi kita, walau masih belum ada isinya.

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb
$ heroku create laravellia
Creating ⬢ laravellia... done
https://laravellia.herokuapp.com/ | https://git.heroku.com/laravellia.git
```

![1668157029653](image/heroku/1668157029653.png)

heroku create berhasil ☝🏻

# Menambahkan Procfile

Buat file yang bernama `Procfile `dengan cara ketik perintah berikut di terminal didalam folder project Laravel kita.

```bash
touch Procfile
```

![1668157721984](image/heroku/1668157721984.png "procfile")

Setelah itu isi Procfile seperti ini:

```php
web: vendor/bin/heroku-php-apache2 public/
```

![1668157969253](image/Panduan-Heroku/1668157969253.png)

> Kode tersebut berfungsi untuk mengarahkan file indeks aplikasi. Pada laravel, file index.php kan tersimpan di folder public, maka kita mengatur nya di folder public.

**Selanjutnya, inisiasi git dulu didalam folder project (ini bisa *connect* ke github kita juga lho). 😍**

## Initialize Git repo

Jalankan command berikut untuk inisiasi git repo dari terminal *-git remote nya url ke repo masing2 ya.* 🥳

```bash
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/autobot-byte/laravellia.git
git push -u origin main
```

Setelah code naik ke git repo, saatnya kita *setup* persiapan *deploy* ke heroku. 🕺🏻

# Push Aplikasi Ke Heroku

Jalankan perintah berikut:

```
git add .
git commit -m "Add Procfile"
git push heroku master
```

Perintah ini untuk menambahkan file Procfile yang kita buat tadi dan sekaligus mengirim kode aplikasi ke heroku.

Buka [https://dashboard.heroku.com/](https://dashboard.heroku.com/) maka akan ditambahkan otomatis applikasi yang telah kita buat di heroku cli

![1668331857347](image/Panduan-Heroku/1668331857347.png)

Selanjutnya cek **remote git** nya untuk memastikan apakah sudah ada remote bernama **"heroku".** untuk push projek nya ke heroku dengan menggunakan perintah berikut:

Jika responya seperti ini:

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ git remote -v
heroku  https://git.heroku.com/laravellia.git (fetch)
heroku  https://git.heroku.com/laravellia.git (push)
origin  git@github.com:autobot-byte/laravellia.git (fetch)
origin  git@github.com:autobot-byte/laravellia.git (push)
```

maka project kita sudah siap di push ke **Heroku.**

Kemudian push project nya dengan git menggunakan remote yang mengarahkan ke heroku app dengan perintah berikut: 

```bash
git push heroku master
```

Responya:

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ git init
Reinitialized existing Git repository in D:/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb/.git/yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ git add .yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ git commit -m "init"
On branch main
Your branch is up to date with 'origin/main'.nothing to commit, working tree cleanyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ git branch -M mainyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ git push heroku main
Enumerating objects: 141, done.
Counting objects: 100% (141/141), done.
Delta compression using up to 6 threads
Compressing objects: 100% (121/121), done.
Writing objects: 100% (141/141), 326.22 KiB | 8.36 MiB/s, done.
Total 141 (delta 15), reused 0 (delta 0), pack-reused 0
remote: Compressing source files... done.
remote: Building source:
remote:
remote: -----> Building on the Heroku-22 stack
remote: -----> Determining which buildpack to use for this app
remote:  !     Warning: Multiple default buildpacks reported the ability to handle this app. The first buildpack in the list below will be used.
remote:                         Detected buildpacks: PHP,Node.js
remote:                         See https://devcenter.heroku.com/articles/buildpacks#buildpack-detect-order
remote: -----> PHP app detected
remote: -----> Bootstrapping...
remote: -----> Preparing platform package installation...
remote: -----> Installing platform packages...
remote:        - php (8.1.12)
remote:        - apache (2.4.54)
remote:        - composer (2.4.4)
remote:        - nginx (1.22.1)
remote:        NOTICE: detected userland polyfill packages for PHP extensions
remote:        NOTICE: now attempting to install native extension packages
remote:        Installing extensions provided by symfony/polyfill-iconv:
remote:        - ext-iconv (already enabled)
remote:        Installing extensions provided by symfony/polyfill-mbstring:
remote:        - ext-mbstring (bundled with php)
remote:        Installing extensions provided by symfony/polyfill-ctype:
remote:        - ext-ctype (already enabled)
remote: -----> Installing dependencies...
remote:        Composer version 2.4.4 2022-10-27 14:39:29
remote:        Installing dependencies from lock file
remote:        Verifying lock file contents can be installed on current platform.
remote:        Package operations: 70 installs, 0 updates, 0 removals
remote:          - Downloading doctrine/inflector (2.0.6)
remote:          - Downloading doctrine/lexer (1.2.3)
remote:          - Downloading symfony/polyfill-ctype (v1.27.0)
remote:          - Downloading webmozart/assert (1.11.0)
remote:          - Downloading dragonmantank/cron-expression (v3.3.2)
remote:          - Downloading voku/portable-ascii (1.6.1)
remote:          - Downloading symfony/polyfill-php80 (v1.27.0)
remote:          - Downloading symfony/polyfill-mbstring (v1.27.0)
remote:          - Downloading phpoption/phpoption (1.9.0)
remote:          - Downloading graham-campbell/result-type (v1.1.0)
remote:          - Downloading vlucas/phpdotenv (v5.5.0)
remote:          - Downloading symfony/css-selector (v5.4.11)
remote:          - Downloading tijsverkoyen/css-to-inline-styles (2.2.5)
remote:          - Downloading symfony/var-dumper (v5.4.14)
remote:          - Downloading symfony/deprecation-contracts (v2.5.2)
remote:          - Downloading symfony/routing (v5.4.15)
remote:          - Downloading symfony/process (v5.4.11)
remote:          - Downloading symfony/polyfill-php72 (v1.27.0)
remote:          - Downloading symfony/polyfill-intl-normalizer (v1.27.0)
remote:          - Downloading symfony/polyfill-intl-idn (v1.27.0)
remote:          - Downloading symfony/mime (v5.4.14)
remote:          - Downloading symfony/polyfill-php73 (v1.27.0)
remote:          - Downloading symfony/http-foundation (v5.4.15)
remote:          - Downloading psr/event-dispatcher (1.0.0)
remote:          - Downloading symfony/event-dispatcher-contracts (v2.5.2)
remote:          - Downloading symfony/event-dispatcher (v5.4.9)
remote:          - Downloading psr/log (1.1.4)
remote:          - Downloading symfony/error-handler (v5.4.15)
remote:          - Downloading symfony/http-kernel (v5.4.15)
remote:          - Downloading symfony/finder (v5.4.11)
remote:          - Downloading symfony/polyfill-intl-grapheme (v1.27.0)
remote:          - Downloading symfony/string (v5.4.15)
remote:          - Downloading psr/container (1.1.2)
remote:          - Downloading symfony/service-contracts (v2.5.2)
remote:          - Downloading symfony/console (v5.4.15)
remote:          - Downloading symfony/polyfill-iconv (v1.27.0)
remote:          - Downloading egulias/email-validator (2.1.25)
remote:          - Downloading swiftmailer/swiftmailer (v6.3.0)
remote:          - Downloading symfony/polyfill-php81 (v1.27.0)
remote:          - Downloading ramsey/collection (1.2.2)
remote:          - Downloading brick/math (0.9.3)
remote:          - Downloading ramsey/uuid (4.2.3)
remote:          - Downloading psr/simple-cache (1.0.1)
remote:          - Downloading opis/closure (3.6.3)
remote:          - Downloading symfony/translation-contracts (v2.5.2)
remote:          - Downloading symfony/translation (v5.4.14)
remote:          - Downloading nesbot/carbon (2.63.0)
remote:          - Downloading monolog/monolog (2.8.0)
remote:          - Downloading league/mime-type-detection (1.11.0)
remote:          - Downloading league/flysystem (1.1.10)
remote:          - Downloading nette/utils (v3.2.8)
remote:          - Downloading nette/schema (v1.2.2)
remote:          - Downloading dflydev/dot-access-data (v3.0.2)
remote:          - Downloading league/config (v1.1.1)
remote:          - Downloading league/commonmark (2.3.7)
remote:          - Downloading laravel/serializable-closure (v1.2.2)
remote:          - Downloading laravel/framework (v8.83.26)
remote:          - Downloading fideloper/proxy (4.4.2)
remote:          - Downloading asm89/stack-cors (v2.1.1)
remote:          - Downloading fruitcake/laravel-cors (v2.2.0)
remote:          - Downloading psr/http-message (1.0.1)
remote:          - Downloading psr/http-client (1.0.1)
remote:          - Downloading ralouphie/getallheaders (3.0.3)
remote:          - Downloading psr/http-factory (1.0.1)
remote:          - Downloading guzzlehttp/psr7 (2.4.3)
remote:          - Downloading guzzlehttp/promises (1.5.2)
remote:          - Downloading guzzlehttp/guzzle (7.5.0)
remote:          - Downloading nikic/php-parser (v4.15.1)
remote:          - Downloading psy/psysh (v0.11.9)
remote:          - Downloading laravel/tinker (v2.7.2)
remote:          - Installing doctrine/inflector (2.0.6): Extracting archive
remote:          - Installing doctrine/lexer (1.2.3): Extracting archive
remote:          - Installing symfony/polyfill-ctype (v1.27.0): Extracting archive
remote:          - Installing webmozart/assert (1.11.0): Extracting archive
remote:          - Installing dragonmantank/cron-expression (v3.3.2): Extracting archive
remote:          - Installing voku/portable-ascii (1.6.1): Extracting archive
remote:          - Installing symfony/polyfill-php80 (v1.27.0): Extracting archive
remote:          - Installing symfony/polyfill-mbstring (v1.27.0): Extracting archive
remote:          - Installing phpoption/phpoption (1.9.0): Extracting archive
remote:          - Installing graham-campbell/result-type (v1.1.0): Extracting archive
remote:          - Installing vlucas/phpdotenv (v5.5.0): Extracting archive
remote:          - Installing symfony/css-selector (v5.4.11): Extracting archive
remote:          - Installing tijsverkoyen/css-to-inline-styles (2.2.5): Extracting archive
remote:          - Installing symfony/var-dumper (v5.4.14): Extracting archive
remote:          - Installing symfony/deprecation-contracts (v2.5.2): Extracting archive
remote:          - Installing symfony/routing (v5.4.15): Extracting archive
remote:          - Installing symfony/process (v5.4.11): Extracting archive
remote:          - Installing symfony/polyfill-php72 (v1.27.0): Extracting archive
remote:          - Installing symfony/polyfill-intl-normalizer (v1.27.0): Extracting archive
remote:          - Installing symfony/polyfill-intl-idn (v1.27.0): Extracting archive
remote:          - Installing symfony/mime (v5.4.14): Extracting archive
remote:          - Installing symfony/polyfill-php73 (v1.27.0): Extracting archive
remote:          - Installing symfony/http-foundation (v5.4.15): Extracting archive
remote:          - Installing psr/event-dispatcher (1.0.0): Extracting archive
remote:          - Installing symfony/event-dispatcher-contracts (v2.5.2): Extracting archive
remote:          - Installing symfony/event-dispatcher (v5.4.9): Extracting archive
remote:          - Installing psr/log (1.1.4): Extracting archive
remote:          - Installing symfony/error-handler (v5.4.15): Extracting archive
remote:          - Installing symfony/http-kernel (v5.4.15): Extracting archive
remote:          - Installing symfony/finder (v5.4.11): Extracting archive
remote:          - Installing symfony/polyfill-intl-grapheme (v1.27.0): Extracting archive
remote:          - Installing symfony/string (v5.4.15): Extracting archive
remote:          - Installing psr/container (1.1.2): Extracting archive
remote:          - Installing symfony/service-contracts (v2.5.2): Extracting archive
remote:          - Installing symfony/console (v5.4.15): Extracting archive
remote:          - Installing symfony/polyfill-iconv (v1.27.0): Extracting archive
remote:          - Installing egulias/email-validator (2.1.25): Extracting archive
remote:          - Installing swiftmailer/swiftmailer (v6.3.0): Extracting archive
remote:          - Installing symfony/polyfill-php81 (v1.27.0): Extracting archive
remote:          - Installing ramsey/collection (1.2.2): Extracting archive
remote:          - Installing brick/math (0.9.3): Extracting archive
remote:          - Installing ramsey/uuid (4.2.3): Extracting archive
remote:          - Installing psr/simple-cache (1.0.1): Extracting archive
remote:          - Installing opis/closure (3.6.3): Extracting archive
remote:          - Installing symfony/translation-contracts (v2.5.2): Extracting archive
remote:          - Installing symfony/translation (v5.4.14): Extracting archive
remote:          - Installing nesbot/carbon (2.63.0): Extracting archive
remote:          - Installing monolog/monolog (2.8.0): Extracting archive
remote:          - Installing league/mime-type-detection (1.11.0): Extracting archive
remote:          - Installing league/flysystem (1.1.10): Extracting archive
remote:          - Installing nette/utils (v3.2.8): Extracting archive
remote:          - Installing nette/schema (v1.2.2): Extracting archive
remote:          - Installing dflydev/dot-access-data (v3.0.2): Extracting archive
remote:          - Installing league/config (v1.1.1): Extracting archive
remote:          - Installing league/commonmark (2.3.7): Extracting archive
remote:          - Installing laravel/serializable-closure (v1.2.2): Extracting archive
remote:          - Installing laravel/framework (v8.83.26): Extracting archive
remote:          - Installing fideloper/proxy (4.4.2): Extracting archive
remote:          - Installing asm89/stack-cors (v2.1.1): Extracting archive
remote:          - Installing fruitcake/laravel-cors (v2.2.0): Extracting archive
remote:          - Installing psr/http-message (1.0.1): Extracting archive
remote:          - Installing psr/http-client (1.0.1): Extracting archive
remote:          - Installing ralouphie/getallheaders (3.0.3): Extracting archive
remote:          - Installing psr/http-factory (1.0.1): Extracting archive
remote:          - Installing guzzlehttp/psr7 (2.4.3): Extracting archive
remote:          - Installing guzzlehttp/promises (1.5.2): Extracting archive
remote:          - Installing guzzlehttp/guzzle (7.5.0): Extracting archive
remote:          - Installing nikic/php-parser (v4.15.1): Extracting archive
remote:          - Installing psy/psysh (v0.11.9): Extracting archive
remote:          - Installing laravel/tinker (v2.7.2): Extracting archive
remote:        Package swiftmailer/swiftmailer is abandoned, you should avoid using it. Use symfony/mailer instead.
remote:        Generating optimized autoload files
remote:        > Illuminate\Foundation\ComposerScripts::postAutoloadDump
remote:        > @php artisan package:discover --ansi
remote:        Discovered Package: fideloper/proxy
remote:        Discovered Package: fruitcake/laravel-cors
remote:        Discovered Package: laravel/tinker
remote:        Discovered Package: nesbot/carbon
remote:        Package manifest generated successfully.
remote:        49 packages you are using are looking for funding.
remote:        Use the composer fund command to find out more!
remote: -----> Preparing runtime environment...
remote: -----> Checking for additional extensions to install...
remote: -----> Discovering process types
remote:        Procfile declares types -> web
remote:
remote: -----> Compressing...
remote:        Done: 19.8M
remote: -----> Launching...
remote:        Released v3
remote:        https://laravellia.herokuapp.com/ deployed to Heroku
remote:
remote: Starting November 28th, 2022, free Heroku Dynos, free Heroku Postgres, and free Heroku Data for Redis® will no longer be available.
remote:
remote: If you have apps using any of these resources, you must upgrade to paid plans by this date to ensure your apps continue to run and to retain your data. For students, we will announce a new program by the end of September. Learn more at https://blog.heroku.com/next-chapter
remote:
remote: Verifying deploy... done.
To https://git.heroku.com/laravellia.git[new branch]      main -> mainyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$
```

Projek laravel telah di deploy, lalu buka aplikasinya sebagai contoh: [https://laravellia.herokuapp.com/](laravelia) atau bisa juga mengetikan perintah:

```bash
heroku open
```

# Konfigurasi laravel di heroku

Kita perlu definisikan *variable environment laravel* pada *heroku*, caranya tinggal samakan saja *key* yang dibutuhkan pada *file .env* di *heroku cli*, seperti pada command berikut sesuai kebutuhan:

```bash
heroku config:add APP_DEBUG=true
heroku config:add APP_KEY=base64:A1GSHY1C2PTFJa45/h0lEmoXShwac/esnYD2b5Jsn2s=
heroku config:add APP_NAME=laravellia
heroku config:add APP_ENV=production
heroku config:add APP_URL=https://laravellia.herokuapp.com/
```

Selanjutnya jalankan kode ini untuk menambah `APP_KEY` ke environment heroku :

```bash
heroku config:set APP_KEY=$(php artisan --no-ansi key:generate --show)
```

Responnya:

![1668323766544](image/Panduan-Heroku/1668323766544.png)

# Konfigurasi Database di Heroku

Konfigurasi database bisa menggunakan *MySQL* datau *PostgreSQL* di heroku caranya kita perlu install *addon database* yang akan kita pakai, disini kita akan menggunakan database PostgreeSQL karena PostgreeSQL ini  (FREE).

Jalankan perintah berikut ini untuk membuat database baru di heroku.

```bash
heroku addons:create heroku-postgresql:hobby-dev
```

Responya:

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ heroku addons:create heroku-postgresql:hobby-dev
Creating heroku-postgresql:hobby-dev on ⬢ laravellia... free
Database has been created and is available
 ! This database is empty. If upgrading, you can transfer
 ! data from another database with pg:copy
DEPRECATION NOTICE:
 Starting November 28th, 2022, ‘hobby-dev’ databases will no longer be available. To retain your data after this date, upgrade to ‘mini’ or another paid plan. 
 Learn more in our blog (https://blog.heroku.com/new-low-cost-plans)
Created postgresql-triangular-05216 as DATABASE_URL  
Use heroku addons:docs heroku-postgresql to view documentation

ute-1.amazonaws.com port=5432 user=parfbljmlbhsgv password=61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37 sslmode=require"  
Connection URL:   postgres://parfbljmlbhsgv:61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37@ec2-44-195-132-31.compute-1.amazonaws.com:5432/det9j9s7vggsht
```

**Ket: `hobby-dev (adalah nama database-nya: silahkan disesuaikan)`

Selanjutnya kita lihat dulu konfigurasi database yang telah dibuat oleh heroku denga menggunakan perintah berikut:

```
heroku pg:credentials:url
```

Responya:

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ heroku pg:credentials:url
Connection information for default credential.
Connection info string:
   "dbname=det9j9s7vggsht host=ec2-44-195-132-31.compute-1.amazonaws.com port=5432 user=parfbljmlbhsgv password=61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37 sslmode=require"
Connection URL:
   postgres://parfbljmlbhsgv:61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37@ec2-44-195-132-31.compute-1.amazonaws.com:5432/det9j9s7vggsht
```

Atau bisa juga kita cek lewat dasboard: [https://data.heroku.com/]() 

![1668335298828](image/Panduan-Heroku/1668335298828.png)

Selanjutnya sesuaikan *environmentnya* dengan mengguanakan perintah berikut: 

```bash
heroku config:add DB_CONNECTION=pgsql
heroku config:add DB_HOST=ec2-44-195-132-31.compute-1.amazonaws.com
heroku config:add DB_PORT=5432
heroku config:add DB_DATABASE=det9j9s7vggsht
heroku config:add DB_USERNAME=parfbljmlbhsgv
heroku config:add DB_PASSWORD=61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37
```

Responnya: 

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ heroku config:add DB_CONNECTION=pgsql
Setting DB_CONNECTION and restarting ⬢ laravellia... done, v8
DB_CONNECTION: pgsqlyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)

$ heroku config:add DB_HOST=ec2-44-195-132-31.compute-1.amazonaws.com
Setting DB_HOST and restarting ⬢ laravellia... done, v9
DB_HOST: ec2-44-195-132-31.compute-1.amazonaws.comyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)

$ heroku config:add DB_PORT=5432
Setting DB_PORT and restarting ⬢ laravellia... done, v10
DB_PORT: 5432yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)

$ heroku config:add DB_DATABASE=det9j9s7vggsht
Setting DB_DATABASE and restarting ⬢ laravellia... done, v11
DB_DATABASE: det9j9s7vggshtyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)

$ heroku config:add DB_USERNAME=parfbljmlbhsgv
Setting DB_USERNAME and restarting ⬢ laravellia... done, v12
DB_USERNAME: parfbljmlbhsgvyysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)

$ heroku config:add DB_PASSWORD=61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37
Setting DB_PASSWORD and restarting ⬢ laravellia... done, v13
DB_PASSWORD: 61e1cda46a0844ccd34343238f07d36c44be14475229145771067aeb44db5d37yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$
```

Sesuaikan untuk *HOST/DB/USERNAME/PASSWORD* dengan konfigurasi temen-temen.

Setelah selesai konfigurasi variable environmentnya, maka hal yang harus dilakukan adalah *migrate schema database* dan *seedernya. dengan perintah berikut:*

```bash
heroku run php artisan migrate
heroku run php artisan db:seed
```

Respon :

```php
Migration table created successfully.
Migrating: 2014_10_12_000000_create_users_table
Migrated:  2014_10_12_000000_create_users_table (20.79ms)
Migrating: 2014_10_12_100000_create_password_resets_table
Migrated:  2014_10_12_100000_create_password_resets_table (19.31ms)
Migrating: 2019_08_19_000000_create_failed_jobs_table
Migrated:  2019_08_19_000000_create_failed_jobs_table (20.81ms)
Migrating: 2021_05_29_060448_create_blogs_table
Migrated:  2021_05_29_060448_create_blogs_table (15.92ms)

yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$
```

Respon:


```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ heroku run php artisan db:seed
Running php artisan db:seed on ⬢ laravellia... up, run.4522 (Free)
Application In Production!
*Do you really wish to run this command? (yes/no) [no]:yes
Database seeding completed successfully.
```

jika terdapat file uploaded di projek anda, sehingga harus membuat linking ke /public anda bisa saja menggunakan perintah berikut:

```bash
heroku run php artisan storage:link
```

Respon:

```bash
yysofiyan@imac MINGW64 /d/laragon/www/PABWEB-LARAVEL/PABWEB-LARAVEL/21-pabweb (main)
$ heroku run php artisan storage:link
Running php artisan storage:link on ⬢ laravellia... up, run.3131 (Free)
The [/app/public/storage] link has been connected to [/app/storage/app/public].
The links have been created.
```
