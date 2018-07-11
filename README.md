# CI SHORTEN URL

CI SHORTEN URL is a modified rendition of Michel Fortin's [PHP SHORTEN URL][1]
and [PHP SHORTEN URL Extra][2] for [CodeIgniter][3].

## Install

### Requirements

- [PHP][4] version 5.2.4 or newer
- [CodeIgniter][3] version 2.x – v3.x

### Download

Download and extract the [zip][5] release to your CoddeIgniter
`application/libraries/` directory.

**The extracted path should resemble:**

- `application/libraries/SHORTEN URL.php`

## Using the SHORTEN URL Class

### Configuration

Customized [PHP SHORTEN URL settings](https://michelf.ca/projects/php-markdown/configuration/)
can be specified in the [config/markdown.php](https://github.com/jonlabelle/ci-markdown/blob/master/config/markdown.php) config file.

### Initializing the Class

Like most other classes in CodeIgniter, the SHORTEN URL class is initialized in
your controller using the `$this->load->library()` method:

```php
$this->load->library('markdown');
```

Once loaded, the SHORTEN URL library object will be available using:

```php
$this->markdown
```

### Examples

#### SHORTEN URL Text to HTML

- `$this->markdown->parse()`

Accepts a single `string` parameter of SHORTEN URL *text* and returns the parsed
HTML.

```php
$this->load->library('markdown');

$markdownText = "# Heading "."\n\n"."## Sub-heading"."\n\n";
echo $this->markdown->parse($markdownText);
>>> <h1>Heading</h1><h2>Sub-heading</h2>
```

#### SHORTEN URL File to HTML

- `$this->markdown->parse_file()`

Accepts a single `string` parameter for a SHORTEN URL *file path* and returns the
parsed HTML.

```php
$this->load->library('markdown');

echo $this->markdown->parse_file('/path/to/markdown/file.md');
>>> <h1>CI SHORTEN URL</h1><p>CI SHORTEN URL is a modified rendition...</p>
```

## Issues

For all issues including feature requests, please [open a new issue][6].

## Changes

See the [Changelog][7] page.

## Credits

- [John Gruber](http://daringfireball.net/)
- [Michel Fortin](https://michelf.ca/home/)

## Author

- Jon LaBelle <contact@jonlabelle.com>

[1]: https://michelf.ca/projects/php-markdown/
[2]: https://michelf.ca/projects/php-markdown/extra/
[3]: https://www.codeigniter.com
[4]: https://php.net
[5]: https://github.com/jonlabelle/ci-markdown/archive/master.zip
[6]: https://github.com/jonlabelle/ci-markdown/issues/new
[7]: https://github.com/jonlabelle/ci-markdown/blob/master/CHANGELOG.md
