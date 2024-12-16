README: How to Convert a Python Program into a Windows Executable Using auto-py-to-exe
Part 1: English Instructions
Prerequisites
Python Installed: Ensure Python (3.6 or later) is installed on your computer. You can download it from python.org.
Make sure to check the option "Add Python to PATH" during installation.
Pip Installed: Pip is typically included with Python installations. Verify it by running:
pip --version
Install auto-py-to-exe: Install the tool using the following command:
pip install auto-py-to-exe
Check Dependencies: Ensure all Python modules used in your program are installed. Run:
pip install -r requirements.txt
(if you have a requirements.txt file).
Procedure
Run auto-py-to-exe:

Launch the GUI tool by typing the following command in your terminal or command prompt:
auto-py-to-exe
Select Your Script:

In the Script Location field, click Browse and select the Python script (.py) you want to convert.
Choose the Output Settings:

One File: Check this option to bundle everything into a single executable file.
Console/Window Based: Choose:
Console Based: For scripts that require a terminal/command prompt window.
Window Based: For GUI applications that do not need a terminal.
Advanced Options (Optional):

Add Files: If your script depends on external files (e.g., images, configuration files), add them under the "Additional Files" section.
Icon: To add a custom icon to your executable, specify an .ico file in the Icon field.
Arguments: If your program requires command-line arguments, you can specify them under Additional Arguments.
Generate the Executable:

Click the Convert .py to .exe button. The tool will process your script and create the executable.
The output folder will be displayed at the end of the process.
Test the Executable:

Navigate to the output folder and run the .exe file to ensure it works as expected.
Common Issues and Troubleshooting
Missing Modules: If you encounter errors about missing modules, ensure all dependencies are installed:
pip install <module_name>
Executable Size: If the executable is too large, consider using UPX to compress it. Install UPX and enable compression in auto-py-to-exe.
Environment Conflicts: Use a virtual environment to ensure consistent dependencies.
Further Reading
Official auto-py-to-exe documentation: GitHub - auto-py-to-exe
Part 2: Instructions en Français
Prérequis
Python installé : Assurez-vous que Python (version 3.6 ou supérieure) est installé sur votre ordinateur. Vous pouvez le télécharger sur python.org.
Lors de l'installation, cochez l'option "Add Python to PATH" pour inclure Python dans les variables d'environnement.
Pip installé : Pip est généralement inclus avec Python. Vérifiez son installation avec la commande :
pip --version
Installer auto-py-to-exe : Installez l'outil avec la commande suivante :
pip install auto-py-to-exe
Vérification des dépendances : Assurez-vous que tous les modules Python nécessaires pour votre programme sont installés. Utilisez la commande :
pip install -r requirements.txt
(si vous avez un fichier requirements.txt).
Procédure
Lancer auto-py-to-exe :

Ouvrez l'outil graphique en exécutant la commande suivante dans votre terminal ou votre invite de commande :
auto-py-to-exe
Sélectionner votre script :

Dans le champ Script Location, cliquez sur Browse et sélectionnez le fichier Python (.py) à convertir.
Choisir les paramètres de sortie :

One File : Activez cette option pour regrouper tous les fichiers dans un seul exécutable.
Console/Window Based :
Console Based : Pour les scripts nécessitant une fenêtre de terminal/commande.
Window Based : Pour les applications avec interface graphique (GUI) n'exigeant pas de terminal.
Options avancées (facultatif) :

Add Files : Si votre script dépend de fichiers externes (images, fichiers de configuration, etc.), ajoutez-les dans la section "Additional Files".
Icon : Pour ajouter une icône personnalisée à votre exécutable, spécifiez un fichier .ico dans le champ Icon.
Arguments : Si votre programme utilise des arguments en ligne de commande, vous pouvez les ajouter dans Additional Arguments.
Créer l'exécutable :

Cliquez sur le bouton Convert .py to .exe. L’outil va traiter votre script et générer l'exécutable.
Le dossier de sortie sera affiché à la fin du processus.
Tester l'exécutable :

Accédez au dossier de sortie et exécutez le fichier .exe pour vérifier son bon fonctionnement.
Problèmes courants et solutions
Modules manquants : Si vous rencontrez des erreurs concernant des modules manquants, installez-les avec la commande :
pip install <module_name>
Taille de l'exécutable : Si l'exécutable est trop volumineux, utilisez UPX pour le compresser. Installez UPX et activez la compression dans auto-py-to-exe.
Conflits d'environnement : Utilisez un environnement virtuel pour garantir des dépendances cohérentes.
Pour aller plus loin
Documentation officielle de auto-py-to-exe : GitHub - auto-py-to-exe
