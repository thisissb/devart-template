## Example Code
There is an undocumented Google API that seems to fit our bill of exactly what we need. If is a part of the translation API but for our purposes we will just be using it's clever text to mp3 conversion. This will enable us to take tweets from text to sound easily.


```
<?php
 
// Convert Text MP3
// ------------------------------------
 
  $words = substr($_GET['words'], 0, 100);
  $words = urlencode($_GET['words']);
  $file  = md5($words);
  
  $file = "audio/" . $file . ".mp3";
 
   if (!file_exists($file)) {
     $mp3 = file_get_contents(
        'http://translate.google.com/translate_tts?q=' . $words;
     file_put_contents($file, $mp3);
   }
?>
```