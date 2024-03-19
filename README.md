# Proyecto IA udea ai4eng 20241
Proyecto desarrollado para la materia de Modelos y Simulación I, donde se debe evaluar el rendimiento de los estudiantes en las Pruebas Saber Pro. 

# Miembros del grupo
* JONATHAN ANDRÉS GRANDA ORREGO, CC.1001450273, Ingeniería de Sistemas
* JUAN JOSE GARCIA ÁLVAREZ, CC.1152226318, Ingeniería de Sistemas

# Dataset
Los datos usados en el proyecto se toman de la competición [UDEA/ai4eng 20241 - Pruebas Saber Pro Colombia](http://www.kaggle.com/competitions/udea-ai4eng-20241)


Se trabaja en Google Colab, estableciendo una conexión con Kaggle desde el entorno de ejecución.

1. Una vez que hayamos iniciado sesión en Kaggle
   ![image](https://github.com/JGranda11/Proyecto-IA-udea-ai4eng-20241/assets/112766584/9f7d875b-6c15-4621-92be-59368c263423)
   
   Creamos un nuevo token y al descargar el archivo "kaggle.json", es el que nos da las credenciales para usar desde Colab

2. Por lo que ya podemos ejecutar la conexión desde Colab
   ```
     #Necesitamos instalar Kaggle
     !pip install kaggle

     #Cargar el token de Kaggle
     from google.colab import files
     files.upload()
   
   ```
3. Subir el archivo que nos genero el token de kaggle
   
   ![image](https://github.com/JGranda11/Proyecto-IA-udea-ai4eng-20241/assets/112766584/bcc764de-3325-436b-a1b2-828fb653a9cc)
   
4. Ahora debo formar los directorios patra el almacenamiento del proyecto
 ```
     #Crear el directorio desde la raiz
     !mkdir ~/.kaggle
     #Realziar copias del directorio
     !cp kaggle.json ~/.kaggle/
     #Darle el permiso 600
     !chmod 600 ~/.kaggle/kaggle.json
 ```
5. Queremos ahora usar la API, y descargar el dataset, y realizar la extraccion de ficheros
 ```  
   !kaggle competitions download udea-ai4eng-20241
   !unzip udea-ai4eng-20241
```
  Hasta este punto ya tendriamos los datos en el encarpetado del entorno de trabajo de Colab
