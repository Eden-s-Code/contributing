# Contribuciones a Proyectos 🌐

Siguiendo estas pautas, podemos trabajar juntos para mejorar y mantener un código de alta calidad.

!!!☢️Codigo que no cumpla con las normas, será rechazado.

## Cómo Contribuir ❓

Sé respetuoso con otros colaboradores.
Mantén la consistencia con el estilo de codificación existente.
Prueba tu código antes de enviar un Pull Request.
Documenta adecuadamente tus cambios.

### Pasos 
1. **Forkea el Repositorio:** Haz un fork del repositorio a tu cuenta personal y clona tu fork en tu máquina local.

   ```bash
   git clone https://github.com/tuusuario/tuproyecto.git .
   ```

2. Crea una rama para tus cambios
   ```bash
   git checkout -b nombre-de-tu-rama
   ```
   
3. Añade los archivos: Utiliza git add.

   ```bash
   git add .
   ```

4. Haz un Commit: Haz commit de tus cambios de manera descriptiva.

   ```bash
   git commit -m "Añadida nueva característica"
   ```
   
6. Hacer un Push de tu rama: Sube tu rama al repositorio
    ```bash
   git push -u origin nombre-de-tu-rama
   ```
    
7. Hacer un Push: Sube tu rama con los cambios a tu fork.
    ```bash
   git push origin nombre-de-tu-rama
   ```
## Pasos opcionales (Eliminar, Añadir nuevas ramas)

### 8. Si quieres eliminar una rama: sigue estos pasos.

- primero cambiate de rama, ejecuta:
  
  ```bash
   git checkout nombre_de_otra_rama
   ```
- luego ejecuta:
  
  ```bash
   git branch -D nombre_de_la_rama_que_quieres_eliminar
   ```
### 9. Si deseas descargar una rama que se creó después de que descargaste el repositorio, sigue estos pasos:
- primero cambiate de rama, ejecuta:
  
  ```bash
   git checkout nombre_de_otra_rama
   ```
- luego ejecuta:
  
  ```bash
   git checkout -b nombre_de_la_nueva_rama origin/nombre_de_la_nueva_rama
   ```
  
- Con este procedimiento, la rama se creará localmente y se establecerá un vinculo con la rama del repositorio.

10. Por ultimo:
- Crea un Pull Request: Abre un Pull Request desde tu fork a la rama principal del proyecto.

- Revisión del Código: Tu Pull Request será revisado y discutido antes de ser fusionado a la rama principal.

## Reporte de Problemas ⚙️
Si encuentras un problema o tienes una sugerencia, por favor crea un issue en el repositorio.


## Ramas que usaremos 🌱
⚠️recuerda que no nombrar las ramas correctamente es motivo de rechazo del merge

### "feature/nueva-funcionalidad" 💻
- "feature/" para nuevas características, seguido de "nueva-funcionalidad", el cual es el nombre de la funcionalidad. Importante separar con guiones medios.

### "bugfix/correccion-error-123" ❌
- "bugfix/" para correcciones de errores, seguido de "correccion-error-123", el cual es el nombre del error que se solucionó. Importante separar con guiones medios.
- Esta rama se debe crear y cuando se solucione el error debe ser eliminada

### "hotfix/arreglo-urgente" 🔥🛠️
"hotfix/" para arreglos rapidos y urgentes de solucionar, seguido de "arreglo-urgente", el cual es el nombre del error que se solucionó. Importante separar con guiones medios.
- Esta rama se debe crear y cuando se solucione el error debe ser eliminada
- Adicionalmente en esta rama se debe realizar un "REBASE" y NO un "MERGE"
  
### "task/mejora-documentacion" 📎📓
- "task/" para cambiar la documentacion del proyecto, seguido de "mejora-documentacion", el cual es el nombre de los que se cambio. Importante separar con guiones medios.

### "develop" 🧑‍💻
- Esta rama será utilizada como un "main" para el desarrollo
- Los pull request seran opcionales en esta rama, pero se recomienda su uso

### "main" 👑
- Esta es la rama principal del proyecto y la que se usará para realizar el despliegue a producción
- En esta rama es obligatorio el uso de pull request y los push directos serán bloqueados


# Como usamos javascript 

## Declaración de variables
- Usamos camelCase para nombrar a las variables
- Evitar cualquier otra forma de nombrar variables
- Evitar uso de la declaracion var en variables

### Ejemplo (Evitar) ❌
```js
   var esta_es_m_variable = 2;
   const EstaEsMiVariable = 2;
```

### Ejemplo ✅
```js
   let estaEsMiVariable = 2;
```

## Funciones

### Preferimos utilizar esta sintaxis para las funciones, a menos que sea obligatorio emplear la forma tradicional.
```js
   let uno = 1;
   let dos = 2;
   const miFuncion = async (parametroUno, parametroDos)=>{
       //aqui va la logica de la funcion
       console.log("funcionamiento");
   }

   miFuncion(uno,dos);
```

## Importación de librerias (ES6)

### Evitar commonJs ❌
```js
   const elem = require('module');
   module.exports = {
   };
```

### Preferimos utilizar la sintaxis de ES Modules ✅
```js
   import {elem} from './module.js'
   const elem1 = async () =>{
   }

   const elem2 = async () => {
   }

   export = {elem1,elem2};
```

## Uso de React (Vite js) 🖥️
- La estructura completa de nuestros proyectos estara en un repositorio.
- Nuestro enfoque al momento de implementar css es a través de "styled-components", asi que uno de nuestros componentes se veria asi.

### Ejemplo
```js
   import styled from "styled-components";

   const Form = styled.form`
       display: flex;
       flex-direction: column;
       padding: 1rem;
       background-color: aqua;
   `;


   function PayForm() {   
       return (
           <>
               <Form>
               </Form>
           </>
       );
   }
   
   export default PayForm;

```

# Rutas que usaremos 🛣️
- Considerar que para mayor seguridad algunas rutas estaran en variables de entorno y se recomienda su uso
- Las rutas reales pueden variar y dependen de cada proyecto, esto es un ejemplo.

## GET

### "/" (Ruta principal)
- Index de la pagina

### "/sobre-nosotros"
- Ruta para la información de los clientes

### "/contacto"
- Ruta de contacto de los clientes

### "/productos"
- Debe mostrar todos los productos
    #### "/productos/codigo-o-nombre-del-producto"
    - Debe mostrar un producto especifico


## POST (Todos los retornos son en formato JSON)

### "/email"
- Debe encargarse de los envios de correos. Si tiene exito debe devolver true de lo contrario devolver false 

### "/productos"
- Debe devolver todos los productos 
