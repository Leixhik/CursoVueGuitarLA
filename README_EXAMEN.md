# Examen Teórico de Repaso: Proyecto GuitarLA - Carrito de Compras en Vue.js

Este examen es para practicar y repasar los conceptos aprendidos hasta ahora en el desarrollo del proyecto GuitarLA con Vue.js. Responde las siguientes preguntas para reforzar tu conocimiento.

## Preguntas

1. ¿Qué es Vite y para qué se utiliza en un proyecto Vue.js?
R: Vite es una extensión de Vue Js que nos permite inicializar un proyecto ya configurado y con las herramientas que deseemos, incluso herramientas diferentes que Vue como React, etc.

**Retroalimentación:**
Vite no es una extensión, es un "bundler" o herramienta de construcción moderna que permite crear proyectos rápidamente, con recarga en caliente y configuración mínima. Sirve para iniciar proyectos Vue.js (y otros frameworks) de forma eficiente.

2. ¿Qué es un Single File Component (SFC) en Vue.js?
Es un archivo tipo .vue que tiene 3 tipos de información en donde va el HTML, CSS y JS

**Retroalimentación:**
¡Correcto! Un SFC es un archivo `.vue` que contiene la estructura (template), estilos (style) y lógica (script) de un componente en un solo archivo.

3. ¿Cuáles son las tres secciones principales de un archivo `.vue`?
<template> <style> y <script>

**Retroalimentación:**
¡Correcto! Son `<template>`, `<script>` y `<style>`.

4. ¿Para qué sirve la extensión Volar en VS Code?
Para poder visualizar mejor los componentes de Vue

**Retroalimentación:**
Volar es una extensión que mejora el soporte de TypeScript, autocompletado, y validación de código en proyectos Vue. No cambia la visualización, pero sí la experiencia de desarrollo.

5. ¿Qué diferencia hay entre `ref` y `reactive` en Vue.js?
Ref es para multiples objejos, como arrays, y reactive más para objetos individuales, pero ambos pueden trabajar similarmente

**Retroalimentación:**
La diferencia principal es que `ref` se usa para valores primitivos (números, strings, booleanos) y también para objetos/arrays, pero siempre accediendo con `.value`. `reactive` se usa para objetos y arrays completos, y los hace reactivos directamente. Ambos pueden usarse para objetos, pero su uso recomendado es diferente.

6. ¿Cómo se define una variable reactiva usando `ref`?
const objeto = ref([])

**Retroalimentación:**
¡Correcto! Así se define una variable reactiva con `ref`. Recuerda que para acceder/modificar su valor se usa `.value`.

7. ¿Cómo se define un objeto reactivo usando `reactive`?
const objeto = reactive({
    ...
})

**Retroalimentación:**
¡Correcto! Así se define un objeto reactivo con `reactive`.

8. ¿Qué es el state en Vue.js y por qué es importante?
No recuerdo si era basicamente algo como una tipo plantilla que nunca cambia

**Retroalimentación:**
El state es el "estado" reactivo de un componente, es decir, los datos que pueden cambiar y que afectan lo que se muestra en pantalla. Es importante porque permite que la interfaz se actualice automáticamente cuando los datos cambian.


9. ¿Cómo se importan y utilizan componentes en Vue.js?
No recuerdo si es import {  } from 'vue'

**Retroalimentación:**
Para importar un componente se usa: `import NombreComponente from './ruta/NombreComponente.vue'` y luego se registra en el componente padre (en Options API en `components`, en Composition API solo se importa y se usa en el template).

10. ¿Qué es una prop en Vue.js y cómo se define en un componente hijo?
Prop es basicamente como una macro, nos permite realizar acciones en automático ya definidas, olvidé como definirla en un componente hijo pero creo que primero es definirla como const y usar propt para darle el valor que utilizaremos como objeto, después es utilizar un Compontente definido e implementarlo en donde queremos del HTML

**Retroalimentación:**
Una prop es una "propiedad" que permite pasar datos de un componente padre a un hijo. En Composition API se define con `defineProps({ nombreProp: tipo })` y en Options API con la opción `props: ['nombreProp']`.

11. ¿Cómo se pasan datos de un componente padre a un componente hijo?
No recuerdo, apenas lo voy a empezar a ver

**Retroalimentación:**
Se pasan usando atributos en el template: `<ComponenteHijo :prop="valor" />`. El hijo debe definir esa prop para recibir el dato.

12. ¿Qué hace la directiva `v-for` en Vue.js?
Es básicamente un forEach que nos permite recorrer una lista de objetos, esto con la finalidad de no tener que harcodear tanto HTML

**Retroalimentación:**
¡Correcto! `v-for` permite iterar sobre arrays u objetos y renderizar elementos dinámicamente en el template.

13. ¿Cómo se itera sobre un array en el template de un componente?
v-for:array in "template"

**Retroalimentación:**
La sintaxis correcta es: `v-for="item in array"` dentro de un elemento del template, por ejemplo: `<li v-for="guitarra in guitarras">{{ guitarra.nombre }}</li>`

14. ¿Qué es el Composition API en Vue.js?
Composition en la mejor manera de poder colocar información extraida en el HTML, o eso recuerdo

**Retroalimentación:**
El Composition API es una forma de organizar y reutilizar la lógica de los componentes usando funciones como `setup`, `ref`, `reactive`, etc. Permite mayor flexibilidad y reutilización de código.

15. ¿Cuál es la diferencia entre Composition API y Options API?
Para empezar su sintaxis, la de Options es más para cosas sencillas o más legacy, y actualmente se recomienda más Composition API.

**Retroalimentación:**
Correcto en cuanto a la sintaxis. Options API usa opciones como `data`, `methods`, `computed`, mientras que Composition API usa funciones y variables dentro de `setup()`. Composition API es más flexible y recomendado para proyectos nuevos.

16. ¿Cómo se utiliza la función `onMounted` y para qué sirve?
Basicamente es un callback que se activará al ser montado en el HTML

**Retroalimentación:**
¡Correcto! Se usa dentro de `setup()` para ejecutar código cuando el componente ya está montado en el DOM.

17. ¿Qué hace la función `defineProps` en un componente?
Nos permite definir la macri del props? algo asi recuerdo

**Retroalimentación:**
`defineProps` permite definir las props que el componente hijo recibirá del padre. Es la forma de declarar qué datos espera recibir.

18. ¿Cómo se accede a una prop dentro del template de un componente?
No recuerdo bien, se que era algo asi: 
<Guitarra
    :guitarra = "guitarra"
/>

**Retroalimentación:**
En el template del hijo, se accede usando `{{ nombreProp }}`. En tu ejemplo, sería `{{ guitarra.nombre }}` si la prop se llama `guitarra`.

19. ¿Por qué es importante el atributo `key` al usar `v-for`?
Eso lo desconozco, necesito estudiarlo

**Retroalimentación:**
El atributo `key` ayuda a Vue a identificar cada elemento de la lista de forma única, mejorando el rendimiento y evitando errores al actualizar la lista.

20. ¿Cómo se estructura el flujo de datos entre los componentes en el proyecto GuitarLA?
Se crea una carpeta en src para los componentes, y dentro de la carpeta components van nuestros componentes.vue, los cuales son importados en el App.vue

**Retroalimentación:**
Correcto en cuanto a la estructura de carpetas. El flujo de datos es: App.vue (padre) pasa datos a los componentes hijos usando props.

---

¡Éxito en tu repaso!