En este apartado se encontrarán 7 apartados donde la finalidad es tener una estructura según seá el problema.

Ellos son: regresión, clasificación multiple, clasificación binaria, time series, clusterización, NLP. Sumado a esto, sumaremos un glosario de conceptos y nuevos conceptos a investigar. Y un apartado de problemas comúnes y como solucionarlos


# REGRESION (cashflow abastecimiento, beelo porcentaje de incapacidad )
    # EXPLORACIÓN: 
            # variables continuas: #max, min, media, desvio, distribuciones, percentiles, outliers, nulos, histogramas
            # variables discretas: distribuciones, moda, outliers, nulos
            # relacion entre variables: heatmap correlación, clusterings
    # PROCESAMIENTOS Y FEATURE ENGINEERING: split train test estratificado,Reducción de dimensionalidad
    # MODELOS, ENSAMBES Y SUS PARAMETROS: decisiontreeregressor,randomforestregressor, 
    # AJUSTES POST ENTRENAMIENTO: gridsearch
    # EVALUACIÓN Y METRICAS: absoluto medio (MAE), el error cuadrático medio (MSE) y el coeficiente de determinación (R ^ 2)
    # PROBLEMAS COMUNES
    
# CLASIFICACIÓN MULTIPLE (tematicas efecty)
    # EXPLORACIÓN
    # PROCESAMIENTOS Y FEATURE ENGINEERING: split train test estratificado, Reducción de dimensionalidad
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

# NLP( efecty, santander)
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


# PROBLEMAS COMUNES
problemas clasicos: variables vacias, outliers, desbalance (afecta a train test), correlacion de variables y ruidos, split de dataset, dataset chico
explicación de resultados: LIME
dataset desbalanceado: SMOTE 
dataset chico: modelos simples, ojo outliers, selectivo con los features, ensamble de modelos debiles, SMOTE 