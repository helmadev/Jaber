<h1 align="center"> Jaber </h1>
<h1 align="center"> Laravel auxiliary package for Iranian developers </h1>

I always had a series of codes that every time I created a new project, I would copy them from the beginning in the new project. Then I decided to make this into a package so that both myself and my colleagues could easily use them. Now, if you also think that this package can speed up the development process of your software, you can also use it. If you think that there is something special for Iranian developers, but it is not available in this package, then it is

fork and pull request

Make a guest 😁.

Possibilities:

* Save and retrieve solar date in Eloquent
* Betting on a solar date query
* Middleware to repair K and Arabic letters and Persian and Arabic numbers
* Persian slog preparation function
* Validator of mobile number and fixed contact number
* Database of Iranian cities and provinces along with root bindings
* Find the bank by card number

## Install Package

To install this package, you need Laravel version 6 or higher. To install with Composer, use the following command.

<div dir="ltr">

```bash
composer require helmadev/Jaber
```

</div>

Then you can create Jaber config file with this command.

<div dir="ltr">

```bash
php artisan vendor:publish --provider=Jaber\\JaberServiceProvider
```

</div>

config file in the path:

<div dir="ltr">

```
config/jaber.php
```

</div>

You can change the configuration by editing this file.
If you don't want to use the city and province feature.
Set geo to false.
In this way, the related tables will not be created.

## Save and restore solar date
This package allows you to easily convert the dates in the Laravel model to <a href="https://github.com/hekmatinasser/verta"> Verta </a> class. To begin:

trait

<div dir="ltr">

`Jaber\EloquentHelper`

</div>

Add to the model you want.

<div dir="ltr">

`use Jaber\EloquentHelper;

class User extends Model
{
    use EloquentHelper; // trait
}`

</div>

Then you can easily access the specifications daily. Just add the extension to the desired field

_fa

add.

<div dir="ltr">

`$user = User::where(...)->first();
$user->created_at_fa // as a class Hekmatinasser\Verta\Verta
$user->created_at_fa_f // 1390/1/1
$user->created_at_fa_ft // 1390/1/1 12:00
$user->created_at_fa_ftt // 1390/1/1 12:00:00
$user->updated_at_fa->format("%B %d %Y") // farvardin 01 1390`

</div>

For better management, you can refer to <a href="https://github.com/hekmatinasser/verta"> Verta </a> documentation. You can also use the same method by setting the date.


