GLOSARIO

# CONCEPTOS A INVESTIGAR
    # weack labeling
    # zero-shot
    # NLP
        # BERTopic
        # UMAP - mantiene caracteristicas de clustering. reducción de dimensionalidad
        # HDBSCAN - encuentra zonas densas de documentos
        # top2vec - chunkearsd


conceptos:

# CONFUSION MATRIX
# Accuracy = TP + TN / (TP + TN + FP + FN): cantidad de aciertos sobre total de muestra
# Precision = TP / (TP + FP): cantidad de aciertos de una clase sobre el total predicto de la clase. valor cercano a 1 indica buena capacidad para evitar falsos positivos
# Recall = TP / (TP + FN)  Also known as sensitivity, or True Positive Rate: cantidad de aciertos de una clase sobre la totalidad de la clase. valor cercano a 1 indica buena capacidad para detectar casos positivos
# F1 = 2 * Precision * Recall / (Precision + Recall) : Se utiliza cuando se quiere equilibrio entre recall y precisión. valor cercano a 1 muy buen recall y precisión. cercano a 0, pobre.


data leakage(fuga). revisar que no haya features post predicción
como segmenta un arbol de decisión: por entropia o por indice de gini (nodo a nodo, identifica el feature que mejor segmente y asi va avanzando. gini=0 es que ese segmento es puro de una clase)
    - underfitting (entrenamiento pobre. tengo high bias y low variance) y overfitting (me pase de mambo. tengo low bias pero high variance). Cuando el error de la validación es minimo, es el punto optimo
        - precisión/low variance (dispersión): En el entrenamiento, todas las muestras dan al mismo punto. 
        - exactitud/low bias (posición media): En el entrenamiento, el valor medio coincide con el verdadero valor de la magnitud medida
        - La validación tiene alta precisión/low variance y baja exactitud/low bias: Overfitting. Muchos epochs, valores duplicados en entrenamiento
        - La validación tiene alta exactitud/low bias pero baja precisión/low variance: Underfitting. X ruido de entrenamiento, se entreno poco, muestra chica, 
cross validation: Toma subgrupos del train como validación y lo testea k veces con el mismo modelo. Si el desvio de todos es alto, hay overfitting  
recall:
f1-score:
accuracy:



- MAE (mean_absolute_error/error absoluto medio):El error promedio de las muestras. Es el más intuitivo y el que se usa para reportar. No el más util para trabajar. El valor esta asociado a lo que se esta midiendo.
- MSE (Mean Squared Error/Error cuadrático medio): Representa el error promedio por muestra al cuadrado. Mientras tenga más outliers o valores atípicos, mas castigará a este kpi y mas grande será del MAE. Efecto contrario si todos los errores son muy pequeños, terminará siendo más pequeño que el MAE.
- RMSE (Root Mean Squared Error/Raiz Error cuadrático medio):Es la raiz de MSE. El error promedio x muestra. Como el MAE, pero castigado por outliers o errores groseros. misma logica que mse, pero se lo puede relacionar aún más con el valor.    
R2/coefficient of determination: 1-(MSE(vs valor real) / MSE(vs media)). MSE(vs media): Es el error más ingenuo y simplista, suponiendo que el modelo a predecir siempre será la media.
    Es una comparación de MSE vs el MSE de un modelo simplista de la media. Da una idea de cuan bien estoy vs este MSE de referencia. si es cercano a 1, esta muy bien. Si es igual que cero, el modelo es lo mismo que predecir siempre la media. Si R2 es negativo, conviene utilizar la media que el modelo para predecir (modelo malísimo).
    El problema es que si agrego variables, siempre va a acercarce a 1. No considera el ruido como un problema! sino como ayuda a disminuir el error.
R2 ajustado. Lo mismo que el R cuadrado, pero con una diferencia: El coeficiente de determinación ajustado penaliza la inclusión de variables.
MSPE – Error de porcentaje cuadrático medio
MAPE – Error porcentual absoluto medio
RMSLE – Error logarítmico cuadrático medio


Distribuciones:
    CONTINUAS
        - Uniforme
        - Normal
        - Gamma
        - chi cuadrado (caso especial de gamma)
        - Pareto
        - t student
                                                                                         
    DISCRETAS
        - Uniforme (1 dado)
        - bernulli (binario, con una proba)
        - Geometrica.La probabilidad de tener un exito en tantos intentos
        - Pascal/Distribución binomial negativa. Cantidad de dias transcurridos 4 fallas de maquina
        - Poisson (Se especializa en la probabilidad de ocurrencia de sucesos con probabilidades muy pequeñas en el tiempo. Ej: falla en maquinas)

hyperparametros: los parametros que no se pueden definir previamente

LIME. Explica clasificaciones de cualquier modelo de ML. como? Inicia generando leves perturbaciones o eliminando features de sample que se quiere explicar, y enviándolo de nuevo al modelo inicial.


    - Redes Neuronales
        - learning_rate, relacionado a optimazer
        - loss: muy parecido al error que voy a medir 
        - optimzer (velocidad de corrección)
        - epochs: qty de iteraciones sobre el train
        - batch: qty de muestras con la que se updatea el error del modelo en el entrenamiento. Mientras más grande el batch, más lento entrena por acumular datos temporales, pero se vuelve más preciso porque ajusta los parametros en base a muestras grandes. Si entrenamos con batch chicos, va a ser mas rapido, pero con menor precisión porque cada ajuste se hace según una muestra chica
        - accuracy: aciertos sobre intentos



weak labeling: cuando el etiquetado no es 100% certero, hay tecnicas para etiquetar
 - Anotación de etiquetas múltiples: a una oración la etiqueto con varias etiquetas
 - Anotación de etiquetas de grado: a una oración la etiqueto con un grado de probabilidad
 - Anotación de etiquetas de región: a una oración solo etiqueto una frase
 - Anotación de etiquetas por partes: etiqueto por frases
 - Anotación colectiva: varios anotadores etiquetan el mismo conjunto de datos 

 Labelbox, Dataloop, VGG Image Annotator, Labelbox, Labelbox, RectLabel, LabelImg, Labelbox, entre otros.





DATA ENGINEERING
Debug/Depuración: Encontrar y eliminar errores
Bug: Error
Castear: dar el formato adecuado
Parsear: Analizar un código XML sintácticamente, y revisar si tiene todos los campos que consideramos obligatorios
Anidar: Relacionar las bases de datos
On premise: trabajar de forma local (contrario a trabajar en la nube
