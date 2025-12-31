# lab-3
**Étape 1 : Initialisation de DVC dans le projet**


On a préparé le projet pour le suivi et la gestion des fichiers volumineux en utilisant DVC en complément de Git. On a créé et activé un environnement virtuel afin d’installer DVC de manière isolée, puis on a installé et initialisé DVC dans le projet.
<img width="910" height="452" alt="image" src="https://github.com/user-attachments/assets/495612cd-f8a7-40ac-b05e-32bd2dc0e16c" />
<img width="782" height="462" alt="image" src="https://github.com/user-attachments/assets/2989d552-084e-494d-9b35-09c847c5d466" />


**Étape 2 : Versionner les données brutes avec DVC**

On a versionné le dataset brut raw.csv en utilisant DVC afin d’éviter d’alourdir le dépôt Git. On a ajouté le fichier au suivi DVC, ce qui a permis de générer un fichier de métadonnées .dvc et d’indiquer à Git d’ignorer le fichier de données réel. Ensuite, seules les métadonnées et le fichier .gitignore ont été versionnés avec Git. Grâce à cette approche

<img width="954" height="267" alt="image" src="https://github.com/user-attachments/assets/1036f24d-e99b-4f55-b580-a0af7fd0af2a" />
<img width="971" height="236" alt="image" src="https://github.com/user-attachments/assets/cb793614-542a-4f61-86b7-04898d26ed28" />


**Étape 3 : Configuration d’un remote DVC**
