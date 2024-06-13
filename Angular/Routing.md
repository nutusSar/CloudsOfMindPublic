---
tags:
  - "#Angular"
---
## Definition
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
