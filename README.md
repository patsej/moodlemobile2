Moodle Mobile
=================

This is the primary repository of source code for the official Moodle Mobile app.

* [User documentation](http://docs.moodle.org/en/Moodle_Mobile)
* [Developer documentation](http://docs.moodle.org/dev/Moodle_Mobile)
* [Development environment setup](http://docs.moodle.org/dev/Setting_up_your_development_environment_for_Moodle_Mobile_2)
* [Bug Tracker](https://tracker.moodle.org/browse/MOBILE)
* [Release Notes](http://docs.moodle.org/dev/Moodle_Mobile_Release_Notes)

License
-------

[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0)

Big Thanks
-----------

Cross-browser Testing Platform and Open Source <3 Provided by [Sauce Labs](https://saucelabs.com)

![Sauce Labs Logo](https://user-images.githubusercontent.com/557037/43443976-d88d5a78-94a2-11e8-8915-9f06521423dd.png)


Configuration
-------------
Colors
in src/configconstants.ts

* statusbarbgandroid: status bar color for Android
* statusbarbgios: status bar color for iOS
* notificoncolor

Build
-------

```
nvm use 11.12.0
npm run ionic:serve
```

generate the icons run
```
ionic cordova resources
```

www/google-services.json's package_name must match www/config.xml's one

Troubleshooting
-----
Not using npm v 11.12.0 before doing ionic serve, may lead to 
```
[npm] Node Sass does not yet support your current environment: Linux 64-bit with Unsupported runtime (72)
[npm] For more information on which environments are supported please see:
[npm] https://github.com/sass/node-sass/releases/tag/v4.11.0
[npm] npm ERR! code ELIFECYCLE
[npm] npm ERR! errno 1
[npm] npm ERR! moodlemobile@3.8.0 ionic:serve: `npx gulp watch & npx ionic-app-scripts serve -b --devapp --address=0.0.0.0 "--address" "localhost" "--port" "8100" "--livereload-port" "35729" "--dev-logger-port" "53703" "--nobrowser"`
[npm] npm ERR! Exit status 1
```