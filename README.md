# HMS-AutoPyTorch

TODO copia descrizione da file google docs

## Getting started

E' possibile visualizzare i notebook su kaggle con i link nelle rispettive sezioni.

Tuttavia, se si desidera eseguire il codice sulla propria macchina, è necessario
* installare le librerie necessarie per l'esecuzione del codice
* scaricare i dataset utilizzati dai notebook su kaggle (si possono scaricare dai notebook stessi)

### CatBoost

Il link per il notebook di Kaggle è disponibile [qui](https://www.kaggle.com/code/alessandroisceri/catboost-hms).

Nel caso non fosse già installata, si può scaricare la libreria tramite il seguente comando

```python
  pip install catboost
```

Nel caso non si disponga di una GPU, è possibile modificare la seguente porzione di codice

https://github.com/Alessandro-Isceri/HMS-AutoPyTorch/blob/09c39f8b5f3970eebbfdfc6c7c0a889a8c006f71/src/HMSCatBoost.py#L161-L168

Sostituendo 
```python
    task_type="GPU",
    devices='0:1'
```
con
```python
    task_type="CPU"
```

### AutoPyTorch

Il link per il notebook di Kaggle è disponibile [qui](TODO METTI LINK KAGGLE AUTOPY).

Nel momento in cui è stato sviluppato questo progetto, la normale installazione di AutoPyTorch
