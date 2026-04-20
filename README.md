![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)


# Progetto Calcolatori Elettronici
Progetto focalizzato sull'analisi di vari modelli di Motion Capture Markerless. 
I modelli utilizzati sono basati su diverse pipeline di Machine Learning per l'esecuzione in tempo reale: 
      - MoveNet: Analisi delle varianti Lightning, Thunder e MultiPose; 
      - MediaPipe Holistic: Ricostruzione integrale di corpo, mani e volto; 
      - YOLOv8 + MediaPipe : Approccio sperimentale di unione tra l'object                 detection YOLOv8 per il multitracking multi-persona con la stima della             posa di MediaPipe


La nostra analisi è stata condotta interamente su **CPU**, a causa di vincoli con le librerie Metal. 
Nella documentazione abbiamo analizzato in generale le architetture ARM, analisi di performance dei MacBook M1 e M3. 


## Struttura Repository

· /models : Contiene i modelli pre-addestrati 

· /notebooks : Jupyter Notebook con il codice di ogni modello 

· /Documentazione: Analisi tecnica completa e bibliografia. 

## Autori
**Rebecca Spiga** - [Profilo GitHub](https://github.com/kimtaejin220-dev)  
- Contributo: 

**Francesco Roberto Terrosu** - [Profilo GitHub](https://github.com/FrancescoTerrosu)  
- Contributo: 


