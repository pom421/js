#### Divers

- Doc 
 - https://api.jquerymobile.com/category/reference/ : référence des attributs data
 - https://api.jquerymobile.com/category/widgets/ : référence des widgets
 - http://demos.jquerymobile.com/1.4.5/ : démos de tous les widgets
 - https://themeroller.jquerymobile.com/ : theme roller


- data-theme : permet de préciser la nuance (entre a et z) du thème créé par Theme Roller = swatch
- font squirrel : pour transfrormer une police en police css

- font awesome ou glyphicons (mais ce dernier n'est pas SVG en mode libre de droit sauf si intégré avec Bootstrap)

- https://build.phonegap.com : gratuit si projet public

- phone gap developer : app smarpthone pour récupérer des app de Phone gap build

- chrome inspect (faire chrome://inspect) pour faire du remote debugging (utiliser Safari pour une app iPhone)

- native droid : material design Android pour jQuery Mobile

- framework 7 : "successeur" de jQuery Mobile
 
- codiqa : pour faire un prototype rapide en jQuery Mobile (payant)

- class=ui-state-persist pour conserver le focus quand on clique sur un navbar (ne pas intégrer un navbar dans un footer...)

- Nested view : ne fonctionnent plus depuis la version 1.4

- JQM prend la main après l'affichage pour y mettre son traitement. Par exemple, cela a pour effet de faire perdre le focus à un input. Pour le fixer à nouveau, soit récupérer après l'évènement pagecreate, cad pageshow. Si ça ne marche pas : 

````
  setTimeout(function(){
    $(".ui-filterable input").focus();
  },0);
````

- table : data-role="table" data-mode="reflow" class="ui-responsive">

````
$(window).on("orientationchange", function(e) {
   console.log("orientationchange");
});
````
À faire après le script de jquery mobile (= évènement mobileinit)

####Ionic

- ionic package : permet de créer une app pour Android ou iOs
- ionic creator : outil pour faire des maquettes (// codiqa)
- ionic app view : app servant de container sur ses apps dans le cloud
- ngcordova : plugins cordova wrappés en angular


#### 

- yeoman : utilise des generator. Clic sur Discovering generators
- generator-jquery-mobile
- yo jquery-mobile
- https://webpack.github.io/docs/ : avenir de la gestion de modules JS 
