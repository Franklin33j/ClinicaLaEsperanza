# Clinica La Esperanza

## Descripcion

Clinica la esperanza es un proyecto academico-profesional en el cual se busca crear un software para una clinica para automatizar aspectos como:

- Manejos de consultorios,salas
- Administracion de especialidades
- Administracion de expedientes de pacientes
- Administracion de citas de pacientes

## Tecnologias Usadas

+ BACKEND: Se trabaja con .NET Core 6, en un servidor gratuito de [Render](https://render.com/).Esta alojado atraves de un contenedor usando Docker
+ FRONT END: Se esta trabajando con Vue.js en  [Netlify](https://www.netlify.com/) un servidor para archivos estaticos

## Estado
La api de se encientra ejecutandose, con algunas funciones que se han trabajado:
- Registro/Inicio de sesion
- Especialidades
- Consultorios

Estado: **Ejecutandose**, a veces se cae, por ser gratuito. 

La parte del frontend se ha trabajo el login pero, pero se trabajara para ofrecer el enlace lo mas pronto posible

## Endpoints

### Auth
 - Login(Post):
    https://clinicalaesperanza.onrender.com/api/v1/Auth/Login. Los parametros son:
    
    ```
    {
        "due": "string",
        "password": "string"
    }
    ```
- Register(Post):
    https://clinicalaesperanza.onrender.com/api/v1/Auth/Register.
    
    Proporciona acceso como paciente, (si fuera empleado el administrado debera modificar su rol, o crearlo directamente ). Los parametros son:
    ```
    {
        "firstNames": "string",
        "lastNames": "string",
        "password": "string",
        "due": "stringstr",
        "address": "string",
        "phoneNumber": "string"
    }
  ```


- Refresh Token (Post):
https://clinicalaesperanza.onrender.com/api/v1/Auth/RefreshToken
permite extender el tiempo de acceso de recursos a los usuarios. Los parametros son:
  ```
    {
        "expiredToken": "string",
        "refreshToken": "string"
    }
  ```



