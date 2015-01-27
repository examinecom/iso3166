iso3166
=======

ISO 3166-1 alpha-2 mapping:

```php
echo Iso3166\Codes::map('FR');
// 'France'
```

```php
echo Iso3166\Codes::reverse_map('france');
// 'FR'
```

```php
echo Iso3166\Codes::search('fran');
/* 
Array (
    [0] => Array (
        [FR] => France
    )	
)
*/
```

Plus one super handy helper:

```php
echo Iso3166\Codes::select('class', 'name', 'FR');
```

will output:

```html
<select class="class" name="name">
  <option value="AF">Afghanistan</option>
  ...
  <option value="FR" selected>France</option>
  ...
</select>
```

_How to use with composer_

```javascript
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/kzap/iso3166"
        }
    ],
	"require": {
		"julien-c/iso3166": "dev-master"
	}
}
```
