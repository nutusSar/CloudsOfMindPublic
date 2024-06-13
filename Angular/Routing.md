---
tags:
  - "#Angular"
---
## Funtionsweise
Routing ermöglicht das einfache hin und her wechseln zwischen verschiedenen Bereichen einer Angularanwendung. 
Dafür müssen zuerst Routen definiert werden. Dies geschieht in einem konstanten Array, welches in der **app.module.ts** angelegt wird. In diesem Array befinden sich Instanzen des Routes-Objektes. 
**Beispiel**:
```ts
const appRoutes: Routes = [
  {path: 'path1', component: 'Component1'},
  {path: 'path2', component: 'Component2'},
  {path: 'path3', component: 'Component3'}
]
```
Die angelegten Routen müssen nun Angular bekanntgegeben werden. Dazu wird ebenfalls in der **app.module.ts** unter **imports** ein neuer Eintrag hinzugefügt.
**Beispiel**:
```ts
imports: [
  ...,
  RouterModule.forRoot(appRoutes)
]
```
In dem Template **app.component.html** wird die [[Direktive]] **router-outlet** verwendet, um Angular die entsprechende Stelle zu kennzeichnen, wo die bei den Routen hinterlegte Komponente gerendert werden soll.
**Beispiel**:
```html
<div class="row">  
  <div class="col-xs-12">  
    <router-outlet></router-outlet>  
  </div>
</div>
```


>[!tip] routerLink vs. href
Es empfiehlt sich das Attribut routerLink zu benutzen anstelle von href, denn href hat den Nachteil, dass es eine Request zum Server schickt. Dadurch wird das neu Laden der Angularanwendung erzwungen.
>```html
><a routerLink='/...'></a>
>```


## Visuelle Identifikation
Um z.B. aktuell ausgewählte Routen in einer Navigation visuell zu markieren, kann das Attribut **routerLinkActive** hinzugefügt werden. 
**Beispiel**:
```html
<ul class="nav nav-tabs">  
  <li role="presentation" routerLinkActive="active"><a routerLink="/">page1</a></li>  
  <li role="presentation" routerLinkActive="active"><a routerLink="/page2">page2</a></li>  
  <li role="presentation" routerLinkActive="active"><a routerLink="/page3">page3</a></li>  
</ul>
```

>[!tip] Fehlerhaftes Verhalten
>routerLinkActive übrprüft ob die Route des Elements in der aktuellen Route enthalten ist. So wird page1 und page3 als aktiv markiert, obwohl nur page3 geöffnet ist, denn "/" ist Teil der Route "/page3". Um dies zu verhindern, füge folgende Konfiguration hinzu
>```html
>...
>  <li role="presentation" routerLinkActive="active" 
   [routerLinkActiveOptions]="{exact: true}"><a routerLink="/">page1</a></li>  
>...
>```


