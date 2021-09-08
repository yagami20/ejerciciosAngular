# ejerciciosAngular
ng serve -o 
--> para ejecutar el cli de angular

--
para crear componente 
ng g c --help
ng g c home -is   //-->crea componente 
/* para direccionar un componente se borra la ultima letra del componente 
y se la vuelve a escribir luego presionar tab y listo*/

--
para generar componente dentro de una carpeta
ng g c pages/about/about --flat --skipTests-->sin archivo de pruebas y dentro de un directorio

ng g c contact --flat -is --skipTests /* de esta manera se crea archivos en el directorio raiz */


---crear servicio
ng g s --help -->ver ayuda de servicio (ng g) (s) -->sigla de servicio (c)-->component
ng g s auth -->generar servicios //se puede eliminar el archivo auth.service.spect.ts
los archivos services se pueden mover a una carpeta services sin causar problemas
// se envia mensajes por consola de navegador de la sig manera
export class AuthService {

  constructor() { 
    console.log('hola desde AuthService');
  }
}
//para inyectar un servicio se lo coloca en el constructor de un componente

import { Component} from '@angular/core';
import { AuthService } from 'src/app/services/auth.service';

@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styles: [
  ]
})
export class HomeComponent  {

  constructor(private authService: AuthService) { }

  ngOnInit(): void {
  }

}

//paa crear servicios dentro de la carpeta services
ng g s services/user --dry-run -->para simular lo q va a hacer
ng g s services/user -d --skipTests -->para simular con un solo archivo
ng g s services/user --skipTests -->es el user services

//para ver q genera ng g --help
--generar Gard
ng g guard guard/auth --skipTests -->generar guard 
//los guar son servicios

//para reconstruir y agregar los paquetes se usa:
npm install
