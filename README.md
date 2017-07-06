# Laravel5.4 Event Manage with google calendar
	
	1) composer require mspconcepts/ddscalendar
    2) Add service provider in config/app.php 
            MspPack\DDSCalendar\DDSCalendarServiceProvider::class,
    3) php artisan vendor:publish
	4) php artisan migrate

This will publish file called `laravel-google-calendar.php` in your config-directory with this contents:
```
<?php

return [

    /**
     * Path to a json file containing the credentials of a Google Service account.
     */
    'client_secret_json' => storage_path('app/laravel-google-calendar/client_secret.json'),

    /**
     *  The id of the Google Calendar that will be used by default.
     */
    'calendar_id' => '',

];
```

Read [this blogpost](https://murze.be/2016/05/how-to-setup-and-use-the-google-calendar-api/) to learn how to get the correct values for `client_secret_json` and `calendar_id`.
	
    Now go to ==> http://<YOUR DOMAIN>/admin/calendar