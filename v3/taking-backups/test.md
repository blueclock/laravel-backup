---
title: Associating files
---

You can add associate a file with a model like this:

```php
$newsItem = News::find(1);
$newsItem->addMedia($pathToFile)
         ->toMediaLibrary();
```

The file will now be associated with the news item. Adding a file will move your file to your configured disk.

If you want to preserve the original file, you can call `preservingOriginal`:

```php
$newsItem->addMedia($pathToFile)
         ->preservingOriginal()
         ->toMediaLibrary();
```

<span class="version">v3.8+</span> You can also add a remote file to the media library:

```php
$url = 'http://medialibrary.spatie.be/assets/images/mountain.jpg';
$newsItem->addMediaFromUrl($url)
         ->toMediaLibrary();
```

