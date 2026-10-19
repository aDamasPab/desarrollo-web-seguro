# HackersAnónimos.com

## Integrantes del equipo de desarrollo
| Integrante               | GitHub Nickname |
|--------------------------|-----------------|
| Alejandro Damas          | aDamasPab       |
| Integrante 2             | -               |
| Integrante 3             | -               |
| Integrante 4             | -               |

## Aspectos Principales

### Entidades
- **<u>Post</u>**: entidad que representa los post que créan los usuarios dentro de la web.
- **<u>Comment</u>**: pequeño texto para dar opinión sobre un post en concreto.
- **<u>User</u>**: entidad principal que se encarga de manipular los posts y comentarios.
- **<u>Section</u>**: categorías de los posts.

### Persmisos de los usuarios

- **<u>Admin</u>**: este tendrá control absoluto sobre cualquier entidad. Todo es de su propiedad.

- **<u>User</u>**: podrá crear posts y comentarios, además de poder editar y eliminar todos aquellos que se encuentren bajo su propiedad, es decir, posts y comentarios que haya creado ese mismo usuario. Por otro lado, podrá seguir a otros usuarios e incluso secciones.

### Imágenes
Las entidades con imágenes serán los **Post**, los **User** (foto de perfil) y las **Section** (foto representativa de la sección). Todas estas poseeran máximo una imagen.

### Esquema de la Base de Datos

#### Diagrama 
<img src="Diagrama MySQL.svg" alt="Diagrama de la base de datos generado por MySQL" style="background-color:white; display:block; margin:auto; max-width: 800pxs">

#### Esquema E/R
<img src="Esquema ER.svg" alt="Esquema E/R de las entidades" style="background-color:white; display:block; margin:auto; max-width: 800px">

## Desarrollo Colaborativo

### Alejandro Damas
Encargado principalmente de la clase Post, implementando cada aspecto referente a esta. Además, ha ido manipulando el resto de entidades en mayor o menor medida debido a la conexión de la entidad Post con todas las demás.

#### 5 commits más significativos
- [e7c3c3a](../../commit/e7c3c3a0f7d43a66a46f15ebb6e6c4024de1dd49): se pasa a trabajar con DTOs en PostController y se implementan diversas funcionalidades.
- [eba8e97](../../commit/eba8e978b83eab5070388a522bceabdc181a15d8): se implementan controles de acceso para los diferentes endpoints relacionados con la entidad Post.
- [72cdb19](../../commit/72cdb1955baca8726f6ceca19f0e985d2297f1c8): corrección de errores que impedían la correcta asignación de secciones y colaboradores a los Post. Además de la corrección de un error en el borrado de Post con comentarios.
- [035379e](../../commit/035379e481b6c77a4de12fdbcfb80397a2f6d54e): borrar un post suponía la aniquilación de las secciones a las que perteneciese.
- [223527e](../../commit/223527eeca5ca64663c6e19e4a99788522138061): corrección de errores que provocaban fallos a la hora de visualizar las imágenes de los posts.

#### 5 ficheros en los que más ha participado
- PostService.java
- PostController.java
- PostRestController.java
- PostRepository.java
- SectionService.java

### Integrante 2
Encargada principalmente de la clase Section, implementando cada aspecto referente a esta. Además, ha ido aportando al resto de clases.

#### 5 commits más significativos
- [12d61dc](../../commit/12d61dc229210cf07ef03a5c0e7e28b92effc78d): Todas las entradas de los formularios sanitizadas.
- [ad7e0e9](../../commit/ad7e0e99543ebef640f33f946ac2d0dbe184dff8): Añadido el panel de administrador para que pueda ver todos los usuarios, solo el administrador podrá acceder a esta página.
- [5d72aba](../../commit/5d72aba7de426f03491859cb5da8599710760734): Implementación de JWT y Configuración Detallada de Roles en Spring Security. 
- [06882f6](../../commit/06882f6448b729de9fd44d62d24082024e5cddaf): Implementación de texto enriquecido y securizado en el frontend.
- [83d692a](../../commit/83d692ad929e22c2ee66ccccdbcd94f4f20e824c): Implementación de la consulta dinámica.

#### 5 ficheros en los que más ha participado
- SectionService.java
- SectionRestController.java
- SectionController.java
- SectionRepository.java
- SecurityConfiguration.java

### Integrante 3
Encargado principalmente de la clase Comment, implementando cada aspecto referente a esta como a las entidades relacionadas. Además, ha ido aportando al resto de clases.

#### 5 commits más significativos
- [6ba1ac0](../../commit/6ba1ac04e05523885bd6fe34acf70790259d6338): Implementada el control de acceso para los comentarios
- [708e858](../../commit/708e8589e90af190b4855108e99fba7acafaf025): Implementada la funcionalidad de texto enriquecido
- [6b24d1d](../../commit/6b24d1d1a5afc362106f901c7a04b48b29f44585): Implementado el inicio de sesión de la aplicación
- [dbbdf91](../../commit/dbbdf91cd1d8a4bc15d5c842a2a59d678454e459): Implementada la subida de archivos
- [f6c1344](../../commit/f6c1344cf5010164b66988f9187f13664b0e499a): Implementación del header dinámico para la aplicación

#### 5 ficheros en los que más ha participado
- commentService.java
- userService.java
- postService.java
- SecurityConfiguration.java
- PostRestControler.java

### Integrante 4
Encargado principalmente de la clase User, debida a su alta cantidad de funcionalidad, desarrollada junto con el Integrante 3. 
También ha aportado en cuestiones de seguridad, como control de acceso, content security policy y control de entradas del usuario.

#### 5 commits más significativos
- [7eff891](../../commit/7eff891f5d04a6adfcb32261cd30023c71aa0198) (Implementación del errorHander para errores en API)
- [fa5acad](../../commit/fa5acad69e4b3c502274f09bdbbff62c48eb69fe) contro de acceso usuario api.
- [ce79af4](../../commit/ce79af427aea53aa72cc1005954b657454f188c6) funciones de borrar cv en web y apim y toda la funcionalidad de cv en api
- [8f774c4](../../commit/8f774c4a47b89a92675c5bbf259358ec7fe379c7) Usuario Invitado ya funciona correctamente para ver /home /login y /register
- [8d47ff6](../../commit/8d47ff62b318f32d598d804c7d74dd7d8eeb16f0) ya funciona register, asignando el rol y hasheando la contraseña.

#### 5 ficheros en los que más ha participado
- UserController
- UserRestController
- UserService  
- SecurityConfiguration
- Profile.html