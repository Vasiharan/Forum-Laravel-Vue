# Forum-Laravel-Vue
Forum built using Laravel and Vue


1. Thread
2. Reply 
3. User


# Database seeding

```
php artisan migrate:refresh
php artisan tinker
$threads = factory('App\Thread', 50)->create();
$threads->each(function ($thread) { factory('App\Reply', 10)->create(['thread_id' => $thread->id]); });
```


# CLI Alias
```
alias p='vendor/bin/phpunit'
alias pf='vendor/bin/phpunit --filter'
```