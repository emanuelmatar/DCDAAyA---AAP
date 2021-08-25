# DeepLearning
Práctica Deep Learning

El repositorio cuenta con tres (3) Notebooks desarrolladas en Colaboratory y sus correspondientes archivos de MlFlow. En ellas se prueban los siguientes tres experimentos sobre el dataset del MeLiChallenge del año 2019:

1) CNN sobre la totalidad del dataset: https://colab.research.google.com/drive/1qkkS470CW5vZxDGqXmHVjzV_NW2m_bCQ?usp=sharing
2) CNN sobre un dataset reducido en un órden de magnitud: https://colab.research.google.com/drive/1icfjrmtvigbYJFpHfW81P01E6GaL-vQd?usp=sharing
3) MLP sobre un dataset reducido en un órden de magnitud: https://colab.research.google.com/drive/1vn40E8RGXj7kZAUQB1_bvHqN0zCTZ8vV?usp=sharing

En general, se trabajó sobre un dataset reducido por las limitaciones de hardware que ofrece el Colaboratory. Las pruebas se vuelven tediosas y lentas y un error pequeño de código
puede significar mucho tiempo perdido ya que cada operación sobre los datos conlleva un tiempo considerable.
Pudo correrse el modelo CNN con una baja cantidad de épocas sobre el dataset completo para evaluar la performance vs el modelo sobre el dataset con dataset reducido.
Se usó como parámetro de evaluación del modelo el balanced accuracy (bacc en los notebooks) y se observó:
1) Trabajando sobre el dataset entero con el modelo CNN, el aumento en los valores de bacc es muy bajo de epoca a epoca comparado al esfuerzo computacional que requiere cada época.
2) Trabajando sobre el dataset entero con el modelo CNN y utilizando como función de activación una sigmoide en lugar de una ReLu se obtiene un aumento constante y sostenido del bacc entre iteraciones de epoca de 0.32 a 0.47.
3) En el modelo MLP se ve un aumento constante y sostenido del bacc entre iteraciones de épocas de 0.24 a 0.4.
4) Mlflow con el modelo CNN y aplicado sobre el dataset entero, falla al no ser suficiente la RAM para correr los archivos. Sobre esto se probaron muchas alternativas y lamentablemente no fue factible correr sobre todo el dataset y generar los archivos de mlflow para observar en la UI.
5) Para todos los modelos, en general, se obtienen valores bajos del parámetro, alejándonos del rango óptimo.

Se implementaron modelos reales sobre el dataset. Los problemas centrales tuvieron que ver con la imposibilidad técnica de probar en
tiempo los modelos en Nabucodonosor y el límite de hardware de Colaboratory. También, se observó que el desempeño de los modelos simples como el MLP y CNN con parámetros 
básicos es bastante pobre pero el desempeño del modelo MLP fue notoriamente superior en comparación.
