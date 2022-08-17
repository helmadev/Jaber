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

#Install Package

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

