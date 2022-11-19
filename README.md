# CF-ECS-CI-CD-PIPELINE-TEMPLATE
Cloud Formation template for implement CI/CD Pipeline for deploy ECS Service with LoadBalancer

# Descripcion de algunos de los parametros de la plantilla
- Stage: corresponde a la etapa que se implementara, puede ser desarrollo, qa, prod, entre otros.
- GithubUserName: No hace falta mas detalle pero es el usuario que deberia tener acceso al repositorio que se referencia en el siguiente punto.
- GithubRepo: Este repositorio(recomiendo que sea otro repo) debe contener como minimo un archivo buildspec.yml y los archivos necesarios para correr un servidor web en un contenedor de docker.
Tambien considerar que ese repositorio debe tener una carpeta llamada CloudFormation y dentro de ella debe contener el archivo Fargate-Cluster.yml [ver Fargate-Cluster-Example.yml](Fargate-Cluster-Example.yml), ese archivo es necesario para desplegar la infraestructura de ECS.
- GithubBranch: Corresponde a la rama asociada a la implementacion, debes considerar que si tu "Stage" es "dev", te recomiendo seguir consistentemente con alguna rama que sea de acuerdo a esa etapa, por ejemplo "dev" o "desarrollo"
- GithubOAuthToken: Se puede obtener en tus configuraciones de desarrollador de tu cuenta de github, ten en cuenta que el token debe tener acceso para extraer el codigo fuente del repo GithubRepo.

# Instrucciones de uso
TODO