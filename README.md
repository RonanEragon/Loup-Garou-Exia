# Loup-Garou Exia.Cesi
Création d'un jeu du loup-garou en année A1 à Exia Cesi

## Prerequis

Il vous faudra installer 
- CMake (Ne pas oubier la variable d'environnement à l'installation)
- Git
- Un IDE

## Participer au projet

- Tout d'abord, créez votre propre fork. Votre nom de projet doit être
```
[USER]/Loup-Garou-Exia
```

- Ensuite vous devez cloner votre branche à l'endroit choisi.
Ouvrez la console et tapez
```
git clone --recursive https://github.com/Euxiniar/Loup-Garou-Exia.git
```

- Pour finir, créez un dossier build. Une fois dedans, ouvrez la console et tapez la commande
```
cmake -G "Visual Studio 15 Win64"..
```
Si vous êtes sur Visual Studio 2017,
```
cmake -G "Visual Studio 14 Win64"..
```
Si vous êtes sur Visual Studio 2015, ou
```
cmake -G "CodeBlocks - MinGW Makefiles"..
```
Si vous êtes sur CodeBlocks avec le compilateur MinGW.

### En cas d'erreur
- Avec Visual Studio
Ouvrez Visual Studio installer. Cliquez sur "modifier". Installez le windows 10 SDK (10.0.15063.0) for desktop C++.

- Avec Code::Blocks
Allez dans le dossier [répertoire codeblock]\MinGW\bin, et copier tous les .dll. Collez les dans [répertoire codeblock]\Mingw32\bin

## Contributeurs
* **Euxiniar**

* **Snargol**

* **Ragnay**

* **Trapadore**

* **Anthime-Didi**

* **Hidehal**
