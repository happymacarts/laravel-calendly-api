Calendly API
==========

PHP Calendly API (v2) SDK for Laravel

Installation
------------

Installation using composer:

```
composer require gentor/laravel-calendly-api
```

Configuration
-------------

Change your default settings in `app/config/calendly.php`:

```php
return [
    'personal_token' => env('CALENDLY_PERSONAL_TOKEN'),
    'organization_uri' => env('CALENDLY_ORGANIZATION_URI'),
];
```

Usage
-----

* [Users](https://developer.calendly.com/api-docs/b3A6Mzk2-get-user)

```php
Calendly::users()->me();
Calendly::users()->get();
```

* [Scheduled Events](https://developer.calendly.com/api-docs/b3A6NTkxNDEy-list-events)

```php
Calendly::scheduledEvents()->forOrganization();
Calendly::scheduledEvents()->forUser();
Calendly::scheduledEvents()->invitees();
Calendly::scheduledEvents()->invitee();
```

* [Webhooks](https://developer.calendly.com/api-docs/b3A6NTkxNDI2-list-webhook-subscriptions)

```php
Calendly::webhooks()->list();
Calendly::webhooks()->subscribe();
Calendly::webhooks()->unsubscribe();
```

Documentation
-------------

[Calendly API Docs](https://developer.calendly.com/api-docs)
