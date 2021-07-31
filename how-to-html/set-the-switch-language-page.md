URL  
- [How to get user language](https://stackoverflow.com/questions/8199760/how-to-get-the-browser-language-using-javascript)  
- [What would be the result of window.navigator.userLanguage || window.navigator.language if I run it on browser in Romania](https://stackoverflow.com/questions/40165353/what-would-be-the-result-of-window-navigator-userlanguage-window-navigator-la)  
- [how to display a javascript var in html body](https://stackoverflow.com/questions/40858456/how-to-display-a-javascript-var-in-html-body)
- [Browser Language Detection](https://aruljohn.com/language.php)

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>CollaNote Wiki</title>
</head>
<body>
<h2>Below is the language of your browser</h2>
<p id="language"></p>
<p id="position"></p>

<script type="text/javascript">
    var lang_navuser = navigator.userLanguage;
    var lang_nav = navigator.languages;
    var lang1 = navigator.language || navigator.userLanguage;
    var lang = navigator.languages
    document.getElementById("position").innerHTML = lang.indexOf("vi");
    if (lang.indexOf('vi') == 0)
        //window.location = '/vi/';
        //document.getElementById("language").innerHTML = "Your language Vietnamese...";
    else if (lang.indexOf('ja') == 0)

        //window.location = '/ja/'
        document.getElementById("language").innerHTML = "Japanese";
    else

        //window.location = '/en/';
        document.getElementById("language").innerHTML = "English";

</script>
<script type="text/javascript">
        document.write(lang_nav);
        document.write(lang_navuser);
        document.write(lang1);
        document.write(lang);
</script>

</body>
</html>
```
