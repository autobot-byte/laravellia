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

Follow this steps:

```
 $ git init 

 $ git add .

 $ git commit -m "init"

 $ git branch -M main

 $ git push heroku main
```

* [ ] heroku stuck

---

* check if heroku is added as remote: git remote -v you should see something like this:

heroku [https://git.heroku.com/yourapp.git](https://git.heroku.com/yourapp.git) (fetch) heroku [https://git.heroku.com/yourapp.git](https://git.heroku.com/yourapp.git) (push)

* if there is none then set the remote - git remote add heroku git@heroku.com:MyApp.git (in old git versions ) or heroku git:remote -a example-app (in new version of git)
* git push heroku master (old git) git push heroku main (new git

[https://stackoverflow.com/questions/26595874/heroku-src-refspec-master-does-not-match-any](refernsi)

https://stackoverflow.com/questions/2643502/git-how-to-solve-permission-denied-publickey-error-when-using-git

https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/GitHub-SSH-Windows-Example

---

https://www.niagahoster.co.id/blog/laravel-blog/

https://gilacoding.com/read/contoh-dan-tutorial-project-php-mvc-sederhana-aplikasi-buku-kita

https://afrizalmy.com/

https://balajidharma.medium.com/

https://medium.com/modulr/send-telegram-notifications-with-laravel-9-342cc87b406

https://fahram.dev/article/laravel-8-make-auth

https://programmerindo.com/membuat-login-cepat-dan-mudah-dengan-laravel-8/

https://www.php.id/register.html

---

* [ ] tutorial heroku

https://djiwandou.medium.com/setup-dan-deploy-laravel-project-ke-heroku-b91fdc3aff2

https://bukuinformatika.com/deploy-laravel-ke-heroku/

https://www.ismynr.xyz/2020/10/deploy-laravel-ke-heroku-mysql.html
