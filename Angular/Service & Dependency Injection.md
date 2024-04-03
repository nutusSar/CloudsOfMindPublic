---
tags:
  - Angular
topic: Grundlagen
---
## Service
Services agieren als eine Art zentrales Repository für eine Angular Anwendung. Das heißt, dass wenn Codeduplikate vorliegen, könne diese in einem Service Zentral für alle Komponenten bereitgestellt werden. 
Somit werden Zentrale Funktionen, auf die mehrere Komponenten zugreifen, in einem Service bereitgestellt.

```ts
export class LoggingService() {
	logStatusChange(status: string){
		console.log('A server status cjanged, new status ', status);
	}
}
```
Ein Service besitzt keine Annotation, sondern ist eine normale TS-Klasse. Er wird nicht manuell instanziiert sondern mit einen Dependency Injector. 
## Dependency Injection 
Mit einem Dependency Injector, werden automatisch Abhängigkeiten in Komponenten eingefügt. 
```ts
@Component({
	selector: '',
	templateUrl: '',
	styleUrls: [''],
	providers: [LoggingService]
})
export class NewComponent {
	constructor(priavte loggingService: LoggingService)
}
```
So wird z.B. der LoggingService als eine Abhängigkeit der Komponente hinzugefügt. Als folge wird der LoggingService nit mehr manuell erzeugt, sondern von Angular selbst. 

Es gibt auch die inject() Methode. Doch üblich ist die Dependency injection über den Konstruktor bzw. noch besser über ngOnInit() einer Komponente.

## Hierarchical Injector
+ **AppModule:** Die **selbe** Instanz eines Service ist global in der App verfügbar
+ **AppComponent:** Die **selbe** Instanz eines Service ist für alle Komponenten, aber nicht für andere Services erreichbar.
+ **Jede andere Komponente:** Die **selbe** Instanz ist nur für die Komponente, sowie all ihren Kinder-Komponenten verfügbar.

Niedrigere Ebenen dieser Hierarchie überschreiben die Instanzen der höheren Ebenen für ihren eignen Zuständigkeitsbereich. 
Um jedoch die selbe Instanz zu bekommen, muss der Service aus dem Provider-Array der niedrigeren Ebene der Hierarchie entfernt werden.


## Services in Services
Um einen Service in einen Service zu injizieren, muss dem äußeren eine Annotation hinzugefügt werden. Zudem muss der Service auf der AppModul Ebene bereitgestellt werden. 
```ts
@Injectable()
export class OuterService(){
	constructor(private innerService: InnerService){ }
}
```

Seit Angular 6+ kann man, alternativ zu der AppModule Ebene, auch in der package.jason ein Konfiguration vornehmen. 
```jason
@Injectable({providedIn:'root'})
export class MyService{}
```
