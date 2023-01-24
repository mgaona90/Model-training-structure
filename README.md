En este apartado se encontrarán 7 apartados donde la finalidad es tener una estructura según seá el problema.

Ellos son: regresión, clasificación multiple, clasificación binaria, time series, clusterización, NLP. Sumado a esto, sumaremos un glosario de conceptos y nuevos conceptos a investigar. Y un apartado de problemas comúnes y como solucionarlos


# REGRESION (cashflow abastecimiento, beelo porcentaje de incapacidad )
    # EXPLORACIÓN: 
            # variables continuas: #max, min, media, desvio, distribuciones, percentiles, outliers, nulos, histogramas
            # variables discretas: distribuciones, moda, outliers, nulos
            # relacion entre variables: heatmap correlación, clusterings
    # PROCESAMIENTOS Y FEATURE ENGINEERING: split train test estratificado,Reducción de dimensionalidad (Algorithsms: PCA, SVD, LDA)
    # MODELOS, ENSAMBES Y SUS PARAMETROS: decisiontreeregressor,randomforestregressor, 
    # AJUSTES POST ENTRENAMIENTO: gridsearch
    # EVALUACIÓN Y METRICAS: absoluto medio (MAE), el error cuadrático medio (MSE) y el coeficiente de determinación (R ^ 2)
    # PROBLEMAS COMUNES
    
# CLASIFICACIÓN MULTIPLE (tematicas efecty)
    # EXPLORACIÓN
    # PROCESAMIENTOS Y FEATURE ENGINEERING: split train test estratificado, Reducción de dimensionalidad Algorithsms: PCA, SVD, LDA)
    # MODELOS, ENSAMBES Y SUS PARAMETROS: arboles de decisión (random, xboost, gradientboosting, ), redes (regr log, losso, rasso), SVM, naive bayes, k-NN
    # AJUSTES POST ENTRENAMIENTO: gridsearch, feature importance,  curva ROC (Receiver Operating Characteristic) para selección de corte de umbral
    # EVALUACIÓN Y METRICAS: Curva de aprendizaje, F1-score, AUC para selección de mejor modelo, k-folding(metodo de cross-validation. k=10 es buena): permite verificar si hay overfitting si tienen mucha varianza
    # PROBLEMAS COMUNES:
        explicación de modelos: 	LIME. Explica clasificaciones de cualquier modelo de ML. como? Inicia generando leves perturbaciones o eliminando features de sample que se quiere explicar, y enviándolo de nuevo al modelo inicial.

# CLASIFICACIÓN BINARIA (calculos renales, score crediticio)
    # EXPLORACIÓN: percentiles, histogramas
    # PROCESAMIENTOS Y FEATURE ENGINEERING: split train test estratificado, Reducción de dimensionalidad
    # MODELOS, ENSAMBES Y SUS PARAMETROS: arboles de decisión (random, xboost, gradientboosting, ), redes (regr log, losso, rasso), SVM, naive bayes, k-NN
    # AJUSTES POST ENTRENAMIENTO: gridsearch, feature importance,  curva ROC (Receiver Operating Characteristic) para selección de corte de umbral,
    # EVALUACIÓN Y METRICAS: Curva de aprendizaje, AUC para selección de modelo, confusión matrix para ver: F1-score , recall y accuracy. Curva de aprendizaje, , k-folding(metodo de cross-validation. k=10 es buena): permite verificar si hay overfitting si tienen mucha varianza
    # PROBLEMAS COMUNES:

# TIME SERIES (predicción de demanda USTrading, cashflow abastecimiento)
    # CONCEPTOS:
        #   Componente tendencial: (hay una tendencia en aumento en gral en los últimos 10 años),
        #   Componente cíclica: (comportamientos recurrentes ciclos económicos de 2 o 10 años que se repiten),
        #   Componente estacional: ( causas climatológicas, vacacionales o fiscales, o semanales por alguna razón, menores a la anual) 
        #   Componente irregular: 
    # EXPLORACIÓN:
            #variables temporales: identificación de componentes tendenciales, cíclos, estacionales e irregulares
            # variables continuas: max, min, media, desvio, distribuciones, percentiles, outliers, nulos
            # variables discretas: histogramas, moda, outliers, nulos
            # relacion entre variables: heatmap correlación, clusterings
    # PROCESAMIENTOS Y FEATURE ENGINEERING: split train test estratificado,Redución de dimensionalidad

    # MODELOS, ENSAMBES Y SUS PARAMETROS: modelos de regresión (), alphabet (facebook), ForecasterAutoreg,ForecasterAutoregCustom, CatBoostRegressor, ForecasterAutoregMultiOutput,
    # AJUSTES POST ENTRENAMIENTO:gridsearch
    # EVALUACIÓN Y METRICAS: absoluto medio (MAE), el error cuadrático medio (MSE) y el coeficiente de determinación (R ^ 2)
    # PROBLEMAS COMUNES:

# CLUSTERIZACIÓN (Ustrafing)
    # EXPLORACIÓN:
    # PROCESAMIENTOS Y FEATURE ENGINEERING: Reducción de dimensionalidad, split train test estratificado,
    # MODELOS, ENSAMBES Y SUS PARAMETROS: gridsearch
    # EVALUACIÓN Y METRICAS:
    # PROBLEMAS COMUNES:


PATTERN SEARCH/ Search relations/ ASOCIACION (Ustrafing)
    # EXPLORACIÓN:
    # PROCESAMIENTOS Y FEATURE ENGINEERING: Reducción de dimensionalidad, split train test estratificado,
    # MODELOS, ENSAMBES Y SUS PARAMETROS: gridsearch
    # EVALUACIÓN Y METRICAS:
    # PROBLEMAS COMUNES:


# NLP( efecty, santander)
    # Pasos y conceptos:
    # BoW o contextuales
    # #################Procesos NLP:
# Limpieza (stopwrods, lower, simbols, special characters, diccionarios, corrección ortográfica etc.)
# Tokenización (cada palabra pasa a ser una unidad. la palabra es la unidad minima),
# Lemmatización/stemmatización (busca la relación entre las palabras y busca su raiz madre. ya sea por sufijos/prefijos o mismo verbo por ejemplo. Correr,corren, corri)
# Sequencing (cada palabra pasa a ser un numero)
# Padding,(para el armado de frases, define la dimensión de un vector, tal que si hay menos palabras, pone ceros)
# POS- tagging part of speach (estructura en verbos, sustantivos, etc.),
# Chunking - Process of extracting phrases (chunks) from unstructured text. Identifica frases, que las palabras por si solas significan otra cosa! ejemplo, check out, run out,etc.
# NER (name entity recognition. reconoce persona, entidad, empresa, localidad)
# embedding (cada palabra pasa a ser un vector de X dimensión según la cantidad de palabras. Una red neurnal que tiene de input la sequencia de tokens, y devuelve un vector de 6 dimensiones por ejemplo), 
# DISTANCIAS ENTRE PUNTOS UTILES: cosine_pearson : 0.8280372842978689, cosine_spearman : 0.8232689765056079, euclidean_pearson : 0.81021993884437, euclidean_spearman : 0.8087904592393836, manhattan_pearson : 0.809645390126291, manhattan_spearman : 0.8077035464970413, dot_pearson : 0.7803662255836028, dot_spearman : 0.7699607641618339
# positional encoder (solo para transformers)
    # EXPLORACIÓN: topic_modeling
    # PROCESAMIENTOS Y FEATURE ENGINEERING
    # MODELOS, ENSAMBES Y SUS PARAMETROS
    # EVALUACIÓN Y METRICAS
    # PROBLEMAS COMUNES
    

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





# PROBLEMAS COMUNES
problemas clasicos: variables vacias, outliers, desbalance (afecta a train test), correlacion de variables y ruidos, split de dataset, dataset chico
explicación de resultados: LIME
dataset desbalanceado: SMOTE 
dataset chico: modelos simples, ojo outliers, selectivo con los features, ensamble de modelos debiles, SMOTE 