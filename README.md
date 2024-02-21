# HMS-AutoPyTorch

TODO copia descrizione da file google docs

## Getting started

E' possibile visualizzare i notebook su kaggle con i link nelle rispettive sezioni.

Tuttavia, se si desidera eseguire il codice sulla propria macchina, è necessario:
* Installare le librerie necessarie per l'esecuzione del codice
* Scaricare i dataset utilizzati dai notebook su kaggle (si possono scaricare dai notebook stessi)

### CatBoost

Il link per il notebook di Kaggle che utilizza CatBoost è disponibile [qui](https://www.kaggle.com/code/alessandroisceri/catboost-hms).

Nel caso non fosse già installata, si può scaricare la libreria tramite il seguente comando

```shell
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

Il link per il notebook di Kaggle che utilizza AutoPyTorch è disponibile [qui](https://www.kaggle.com/code/alessandroisceri/autopytorch-hms).

Nel momento in cui è stato sviluppato questo progetto, la normale installazione di AutoPyTorch creava dei problemi con le versioni di python successive alla 3.9.
Per riuscire ad installare e ad utilizzare correttamente AutoPyTorch si può procedere in questi due modi

#### 1) Utilizzo di un virtual environment

Con python 3.9 i problemi creati dalle dipendenze di AutoPyTorch non sussistono, dunque creando un virtual environment si può facilmente risolvere il problema.
```shell
apt-get update
apt install -y python3.9
pip install virtualenv
virtualenv venv -p $(which python3.9)
/venv/bin/pip install autopytorch
```
Nel codice utilizzato in questo progetto è stato necessario anche installare le seguenti librerie per interagire con i file che contenevano i dati
```shell
/venv/bin/pip install pyarrow
/venv/bin/pip install fastparquet
```
Una volta che il setup dell'ambiente di lavoro è terminato, è possibile proseguire salvando il proprio codice in un file python (in questo caso HMSAutoPyTorch.py) ed eseguirlo con il seguente comando
```shell
/venv/bin/python3.9 HMSAutoPyTorch.py
```
#### 2) Installazione di AutoPyTorch tramite git

Grazie all'intervento di un altro utente ([borda](https://github.com/Borda)), che ha modificato le dipendenze come è possibile vedere [qui](https://github.com/automl/Auto-PyTorch/pull/506), è possibile utilizzare il seguente comando per installare AutoPyTorch
```shell
pip install "git+https://github.com/Borda/Auto-PyTorch.git@bump/sklearn-1.0+"
```
### Conclusioni

Una documentazione più approfondita sul lavoro è visualizzabile nel file [TODOnomefile.pdf](inserisciquilink)

