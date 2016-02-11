---
layout: post
title: Простая установка Package Control в Sublime Text
tags: [apache, mysql, php, postgresql, wamp]
---

Проще всего активировать через консоль. Она открывается по нажатию ``Ctrl + ` `` либо через View → Show Console menu.
Далее просто запускаем следующий текст (для Sublime Text 3):

```import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)```
Пост — вольный перевод инструкции https://sublime.wbond.net/installation.