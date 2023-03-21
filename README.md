# Instalacion NPM

Vamos a instalar npm en nuestro proyecto y entender muchos conceptos importantes para el buen funcionamiento de la aplicacion 

## Diferencia entre dependencies vs devDependencies

Las dependencias suelen ser módulos en los que se basa la aplicación para realizar sus funciones principales. Por ejemplo, si estás construyendo una aplicación web, puedes tener dependencias de paquetes como Express, Mongoose o React. Estos paquetes son necesarios para que la aplicación funcione, y deben instalarse cuando la aplicación se despliega en producción.

Por otro lado, las devDependencies son paquetes que se utilizan durante el proceso de desarrollo, como marcos de pruebas como Mocha, o herramientas de formateo de código como Prettier. Estos paquetes no son necesarios para que la aplicación funcione en producción, pero son útiles durante el desarrollo para ayudar a garantizar la calidad y la coherencia del código.

- Instalacion dependencies
```
npm install 'nombre_dependencia'
```
- Instalacion devDependencies
```
npm install 'nombre_dependencia' -D
```


## Instalacion e inicializacion del npm
  
> Con este comando vas a especificar detalle a detalle los parametros a utilizar en tu archivo <b>package.json</b>
```
npm init
```
> Con este comando se pode por defecto los parametros en el archivo <b>package.json</b>

- Ejecucion y modificacion del archivo
  

> Vamos a instalar las dependencias 
Para este caso vamos a instalar la version mas reciente que npm obtenga del repositorio
```
npm i 'nombre_dependencia'
```
Tambien podemos especificar la version a instalar 
```
npm i 'nombre_dependencia'@8.3.1
```

> Modificacion para la ejecucion

"index"-> archivo principal

"nodemon"-> Server local

- Si estamos Usando un servidor local podemos usar <b>dev</b>
```
  "scripts": {
    "start": "node index",
    "dev": "nodemon index"
  },
```

- Si queremos hacer una ejecucion simple podemos usar <b>start</b>
```
  "scripts": {
    "start": "node index",
  },
```


> Ejecucion del proyecto
- Caso 1
```
npm run dev
```
- Caso 2
```
npm run start
```

## Recomendaciones

Ya que la carpeta <b>node_modules</b>, contiene infomacion innecesaria es recomendable no subirlo a tu repositorio

- Crea un archivo <b>.gitignore</b>
- Especifica el archivo a ignorar
```
node_modules
```

## Ejecucion del proyecto

Ha la hora que querer ejecutar el proyecto e intslar las dependencias necesarias para el buen funcionamiento del proyecto, solo necesitamos el <b>package.js</b> y el siguiente comando 
```
npm install
```

## Actualizacion de Paquetes 
Puede ser el caso que vamos a querer altualizar los paquetes a una version mas reciente, para este caso vamos a usar el siguiente comando
```
npm update
```

## Eliminar Modulos 
Puede ver el caso que vamos a eliminar dependencias que no queremos usar, con un simple comando lo podemos hacer

> Si es un devDependencies

```
npm rm 'nombre_dependencia' -D
```

> Si es un Dependencies

```
npm rm 'nombre_dependencia'
```


## Instalacion e inicializacion del npx

Esta forma de instalacion sirve para probar modulos sin instalarlos en nuestra pc o agregarlo a la carpeta de modulos

```
npx cowsay Curso de Node :)
```

## Observaciones

> Si usarmos <b>nodemon</b>, como ejecuble "nodemon index.js", tendremos un error ya que no lo tenemos instalado en nuestra PC, lo que tenemos que hacer es definir la ruta desde el archivo <b>.bin</b> y asi ejecutarlo 

> La otra alternariva es creaer un script usando el modulo, un simple ejemplo seria  ->  "dev": "nodemon index"