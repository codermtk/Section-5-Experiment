# Autoencoder-Based Image Clustering and Visualization

This repository contains the code necessary to train the autoencoder used by AM in:
*"Logic Is Not Universal: Dismantling the Illusion of Reason"*.
It learns latent representations of images and includes clustering with DBSCAN and visualization using UMAP.

Este repositorio contiene el código necesario para entrenar el autoencoder usado por AM en:
*"La Lógica No es Universal: Desmantelando la Ilusión de la Razón"*.
Aprende representaciones latentes de imágenes e incluye clustering con DBSCAN y visualización mediante UMAP.

## Languages / Idiomas

- [English](#instructions-in-english)
- [Español](#instrucciones-en-español)

---

## Instructions in English

### Requirements
1. Install Python 3.8 or higher.
2. Install the required dependencies from `requirements.txt`:
   pip install -r requirements.txt
3. Download the dataset from the following link and place it in the data folder: https://huggingface.co/datasets/gabrielmfr/section4
Example directory structure:

/data10
  ├── clase_1
  │     ├── imagen_0.png
  │     ├── imagen_1.png
  │     └── ...
  ├── clase_2
  │     ├── imagen_0.png
  │     ├── imagen_1.png
  │     └── ...
  └── ...
  
### Usage
1. Dataset Preparation

Place the downloaded dataset in the data10 folder.
Ensure the directory structure matches the example above.
2. Train the Autoencoder

Open the Jupyter notebook and run the cells to train the autoencoder on your dataset.
The training process will save the models as autoencoder_model10.h5 and encoder_model10.h5.
Configuration Options
Batch size: Adjust in the autoencoder.fit method (batch_size=256).
Latent dimension: Update the encoding_dim variable in the autoencoder definition (encoding_dim = 64).
Cluster Latent Representations 

3. The notebook will:

Extract latent representations of images.
Perform clustering using DBSCAN.
Visualize the clusters in 2D space using UMAP.
Visualize New Images

4. Use the update_umap_with_image() function to project a new image into the UMAP space:
new_image_path = "path_to_new_image.png"
new_image = Image.open(new_image_path)
update_umap_with_image(new_image, encoder, dbscan, reducer, X_umap, clusters_dbscan, cluster_to_squares)


## Instrucciones en Español

### Requisitos
1. Instalar Python 3.8 o superior.
2. Instale las dependencias requeridas de `requirements.txt`:
pip install -r requisitos.txt
3. Descargue el conjunto de datos del siguiente enlace y colóquelo en la carpeta de datos: https://huggingface.co/datasets/gabrielmfr/section4

Ejemplo de estructura de directorios:

/data10
  ├── clase_1
  │     ├── imagen_0.png
  │     ├── imagen_1.png
  │     └── ...
  ├── clase_2
  │     ├── imagen_0.png
  │     ├── imagen_1.png
  │     └── ...
  └── ...

### Uso
1. Preparación del conjunto de datos

Coloque el conjunto de datos descargado en la carpeta data10.
Asegúrese de que la estructura del directorio coincide con el ejemplo anterior.

2. Entrenar el autoencoder

Abra el cuaderno Jupyter y ejecute las celdas para entrenar el autoencoder en su conjunto de datos.
El proceso de entrenamiento guardará los modelos como autoencoder_model10.h5 y encoder_model10.h5.
Opciones de configuración
Tamaño del lote: Ajuste en el método autoencoder.fit (batch_size=256).
Dimensión latente: Actualizar la variable encoding_dim en la definición del autoencoder (encoding_dim = 64).
Agrupar las representaciones latentes 

3. El cuaderno:

Extraer representaciones latentes de las imágenes.
Realizar clustering usando DBSCAN.
Visualizar los clusters en el espacio 2D usando UMAP.
Visualizar nuevas imágenes.

4. Utilice la función update_umap_with_image() para proyectar una nueva imagen en el espacio UMAP:
ruta_nueva_imagen = «ruta_a_nueva_imagen.png»
nueva_imagen = Image.open(ruta_nueva_imagen)
update_umap_with_image(nueva_imagen, codificador, dbscan, reductor, X_umap, clusters_dbscan, cluster_to_squares)






