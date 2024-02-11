
Si los textos que cargas desde la feature layer son los que quieres traducir en tu aplicación, lo más recomendable es tener una única feature layer y agregar un campo que indique el idioma de cada texto. De esta manera, podrías cargar todos los textos en la misma capa y filtrarlos según el idioma seleccionado por el usuario.

Para hacer esto, podrías agregar un campo llamado `language` a la tabla de la feature layer, y asignarle el valor `"en"` para los textos en inglés y `"es"` para los textos en español. Luego, en tu aplicación Angular, podrías utilizar el módulo `@ngx-translate/core` para cargar los textos desde la feature layer y mostrarlos en el idioma correcto.

Por ejemplo, podrías definir un servicio que se encargue de cargar los textos desde la feature layer y filtrarlos según el idioma seleccionado por el usuario:

En este ejemplo, se utiliza `TranslateService` de `@ngx-translate/core` para obtener el idioma actual de la aplicación, y se utiliza este valor para filtrar los textos de la feature layer. Luego, se realiza una petición HTTP a la feature layer utilizando `HttpClient` de Angular.


```javascript

import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { TranslateService } from '@ngx-translate/core';

@Injectable({
  providedIn: 'root'
})
export class TextService {
  private url = 'https://services.arcgis.com/.../FeatureServer/0/query';

  constructor(private http: HttpClient, private translate: TranslateService) { }

  getTexts() {
    const language = this.translate.currentLang;
    const params = {
      where: `language = '${language}'`,
      outFields: '*',
      returnGeometry: false,
      f: 'json'
    };
    return this.http.get(this.url, { params });
  }
}

