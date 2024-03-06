# bank-appointment

## Actividad 1: Planificación del Proyecto de Gestión de Turnos para un Banco

### Definición del Proyecto

La aplicación permitirá a los usuarios del banco reservar turnos para diversas gestiones como apertura de cuentas, solicitudes de crédito, asesoramiento financiero, entre otros, evitando esperas innecesarias y optimizando la atención al cliente.

### Requisitos Específicos

- **Autenticación de Usuarios**: Cada usuario debe registrarse y autenticarse para poder reservar un turno. Esto asegura que solo clientes del banco puedan hacer uso del servicio.
- **Tipos de Gestiones**: Los usuarios deben poder elegir el tipo de gestión que desean realizar en el banco para reservar el turno correspondiente.
- **Horario de Atención**: Los turnos deben poder ser reservados dentro de los horarios de atención del banco, considerando también los días laborables y no laborables.
- **Cancelación de Turnos**: Los usuarios pueden cancelar sus turnos hasta 24 horas antes del horario reservado.
- **Notificaciones**: Los usuarios recibirán confirmaciones y recordatorios de sus turnos vía email.

### Extra-Credits

- **Confirmación vía Email**: Implementar un sistema que envíe automáticamente confirmaciones de reserva y cancelación de turnos, así como recordatorios previos al turno.
- **Perfil de Usuario**: Permitir a los usuarios subir una foto de perfil a su cuenta, mejorando la personalización del servicio.

## Actividad 2: Ejecución

### 1. Redacción de User Stories

- **Historia 1**: Como cliente del banco, quiero registrarme e iniciar sesión en la aplicación, para poder reservar, modificar o cancelar turnos.
- **Historia 2**: Como cliente, quiero seleccionar el tipo de gestión bancaria que necesito realizar, para asegurarme de que se me asigne el turno adecuado.
- **Historia 3**: Como cliente, quiero recibir confirmaciones y recordatorios de mis turnos vía email, para mantener un control sobre mis citas programadas.
- **Historia 4**: Como cliente, deseo poder cancelar mi turno con al menos 24 horas de antelación, para reorganizar mi agenda sin inconvenientes.

### 2. Esquema de la Base de Datos

- **Usuarios**: Contiene información de los clientes que utilizan la app.
  - Atributos: `id`, `firstName`, `lastName`, `email`, `password`, `profilePicture` (optional).
- **Turnos**: Registra los turnos reservados por los usuarios.
  - Atributos: `id`, `dateTime`, `typeOfService`, `userId`, `status` (booked, cancelled).
- **TiposGestion**: Enumera los tipos de gestiones disponibles para realizar en el banco.
  - Atributos: `id`, `description`.

Estos pasos cubren la planificación inicial y los esquemas básicos para comenzar el desarrollo de la aplicación de gestión de turnos para un banco. La siguiente fase implicaría el desarrollo del backend y frontend de la aplicación, implementando las funcionalidades descritas en las user stories y siguiendo el modelo de la base de datos establecido.

## Configuración del Entorno TypeScript

### Requisitos Previos

- [Node.js](https://nodejs.org/): necesario para el uso de `npm`.
- TypeScript: Si aún no tienes TypeScript instalado, puedes agregarlo globalmente a tu sistema con `npm install -g typescript`.

### 1. Crea el Proyecto

```
mkdir backend && cd backend
npm init -y
```

### 2. Configura TypeScript

```
tsc --init
```

Configura `tsconfig.json` (opcional):

```
{
    "compilerOptions": {
        "target": "ES5",
        "module": "commonjs",
        "rootDir": "./src",
        "outDir": "./dist",
        "strict": true
    },
    "include": ["src/**/*.ts"],
    "exclude": ["node_modules"]
}
```

### 3. (Opcional) ESLint para TypeScript

```
npm install eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin --save-dev
```

Configura `.eslintrc`:

```
echo '{
"parser": "@typescript-eslint/parser",
"plugins": ["@typescript-eslint"],
"extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended"
]
}' > .eslintrc.json
```

### 4. Escribe Código

Crea un archivo `src/index.ts` y escribe tu código TypeScript.

```
// src/index.ts
console.log("Hello, TypeScript!");
```

### 5. Compila y Ejecuta

```
tsc
node dist/index.js
```

## 6. Scripts en package.json

Añade para facilitar tareas:

```
"scripts": {
    "build": "tsc",
    "start": "node ./dist/index.js",
    "dev": "tsc && node ./dist/index.js",
    "lint": "eslint . --ext .ts"
},
```
