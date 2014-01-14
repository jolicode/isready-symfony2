Si cela n’est pas encore fait, voici le code à insérer dans le head :
```html
<link rel="icon" type="image/png" href="{{ asset('bundles/isreadysite/images/favicon.png') }}"  />
```
Cependant, IE se fait encore remarquer par sa particularité à ne prendre en compte que les favicon au format .ico. Il faudra donc ajouter :
```html
<!--[if IE]><link rel="shortcut icon" type="image/x-icon" href="{{ asset('bundles/isreadysite/images/favicon.ico') }}" /><![endif]-->
```
Plusieurs outils de génération de favicon ont été développés permettant de générer des favicons au format .png ainsi qu’au format .ico ; tels que <a ref="http://favicon-generator.org/" target="_blank">http://favicon-generator.org/</a> ou encore <a href="http://www.favikon.com/" target="_blank">http://www.favikon.com/</a> (quelques exemples parmi beaucoup d’autres).