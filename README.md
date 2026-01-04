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
On a configuré un remote DVC afin de stocker réellement les fichiers volumineux en dehors du dépôt Git. On a d’abord créé un dossier local servant d’espace de stockage pour les données suivies par DVC, puis on l’a déclaré comme remote par défaut.

<img width="944" height="354" alt="image" src="https://github.com/user-attachments/assets/decc6021-c7e2-4faa-802b-f94642a997ec" />
<img width="964" height="191" alt="image" src="https://github.com/user-attachments/assets/bab9c42c-83b7-458e-b9f6-fddba44afdd7" />


**Étape 4 : Push des données dans le remote DVC**

On a simulé la collaboration : on a supprimé le fichier local, puis récupéré exactement le même fichier depuis le remote DVC avec dvc pull. Cela montre que DVC permet de partager et restaurer les données sans surcharger Git.
<img width="627" height="132" alt="image" src="https://github.com/user-attachments/assets/269feae4-fde6-49d7-8df5-2128bc8b9f16" />
<img width="437" height="74" alt="image" src="https://github.com/user-attachments/assets/b2194e25-ad29-4e9d-885e-0dbbb139323c" />



**Étape 5 : imulation d’une collaboration : supprimer localement et récupérer depuis DVC**

On a simulé un scénario de collaboration en supprimant le fichier de données local raw.csv tout en conservant son fichier de suivi .dvc. Ensuite, en exécutant la commande dvc pull, on a récupéré automatiquement le fichier depuis le remote DVC et on l’a restauré à l’identique.
<img width="887" height="328" alt="image" src="https://github.com/user-attachments/assets/bf1248d5-f81d-44e8-b35e-5b333e0ba7c1" />
<img width="966" height="572" alt="image" src="https://github.com/user-attachments/assets/d126b676-410f-4c9e-ade3-c63e12312bb9" />



**Étape 6 : Création d’un pipeline reproductible dvc.yaml**

On a versionné les données transformées et les statistiques d’entraînement avec DVC, en les liant à un commit Git précis.

<img width="1059" height="280" alt="image" src="https://github.com/user-attachments/assets/30a61e5a-e028-4a8d-9d92-90f158b2d242" />
<img width="1244" height="271" alt="image" src="https://github.com/user-attachments/assets/47f93307-c4a7-4edd-b17a-bb9ca32ba05e" />
<img width="1006" height="103" alt="image" src="https://github.com/user-attachments/assets/9f1bd1d8-0156-4705-a141-e438c93fdab9" />


**Étape 7 : Reproduire automatiquement tout le pipeline**

On a structuré tout le workflow de Machine Learning en un pipeline DVC reproductible
<img width="868" height="375" alt="image" src="https://github.com/user-attachments/assets/60bb33af-7749-4a46-aa62-b3ac0b2d6fb0" />
<img width="780" height="587" alt="image" src="https://github.com/user-attachments/assets/8c24c048-9029-47c1-bd94-13b228904ab8" />
<img width="1095" height="133" alt="image" src="https://github.com/user-attachments/assets/d09722d6-d0e0-4d17-9239-78a0c48f3d28" />

la reproductibilité intelligente du pipeline DVC, où dvc repro détecte automatiquement les changements

<img width="1271" height="758" alt="image" src="https://github.com/user-attachments/assets/1840f3a3-f7ab-4511-a490-951768ed1179" />

