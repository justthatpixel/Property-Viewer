# Property Marketplace Coursework

## Project title
AirBnB London Data Set Loader 

## Purpose of project
To load the AirBnB London data set from the provided csv file into a Java data structure

## Authors
KCL Informatics, PPA

## How to import this project in IntelliJ IDEA
1. In the IDEA main menu, select `Import Project` (or `File` → `Open…` if you already have a project open). 
2. Select the project's build.gradle file to import the project.
3. Go to `File` → `Project Structure` → `Project Settings` → `Project` and set `Language level` to `11 - Local variable syntax for lambda parameters`. (This is to ensure Java features that are incompatible with BlueJ won't be used, as BlueJ uses Java 11.)

(Taken and modified from the FabricMC wiki: https://fabricmc.net/wiki/tutorial:setup)

## How to run his project
1. Run in a terminal from the same directory as the project directory `./gradlew run` on GNU/Linux and Mac, or `gradlew run` on Windows.
2. Alternatively, in IntelliJ IDEA, open the Gradle tab on the right and execute `run` under `Tasks` → `application`. After this is done once, you should be able to run the program using the green play button when it is selected as the current run configuration.

(Taken and modified from the FabricMC discord: https://discord.gg/v6v4pMv)

## How to export this project as a BlueJ compatible JAR file
1. Run in a terminal from the same directory as the project directory `./gradlew blueJJar` on GNU/Linux and Mac, or `gradlew blueJJar` on Windows. 
2. Alternatively, in IntelliJ IDEA, open the Gradle tab on the right and execute `blueJJar` under `Tasks` → `build`. After this is done once, you should be able to run the program using the green play button when it is selected as the current run configuration.
3. The JAR should appear in `${projectDir}/build/libs`.
4. If the JAR opens in BlueJ but doesn't compile, you will need to delete all `.class` files in the BlueJ project's root directory, and if that still doesn't work, delete all `.class` files in the whole project. Then create a new JAR file from BlueJ.

(Taken and modified from the FabricMC discord: https://discord.gg/v6v4pMv)

## Additional information

### When an external file is needed (such as CSVs and images)
1. The file should be placed in the `resources` folder, or in a subfolder of it.
2. To reference the file in Java, where `relative/path/of/file` are sub-folders in `resources`:

```java
URL url = getClass().getClassLoader().getResource("relative/path/of/file/filename.someextension");
File file = new File(url.toURI());
```

### When adding text to the application

Use translation keys instead of hardcoding text. To do this in SceneBuilder:
1. Press the gear button next to the text field and click "Replace with Internationalized String".
2. Supply a translation key. For example, the key for the open file button in the start menu is: `button.start.openFile`.
3. To supply the translation for a language, create or locate a file in the folder `resources/bundles` called `lang_bundle_LANGUAGE_CODE`, for example for Great Britain, `lang_bundle_en_GB`.
4. In that file, add a line assigning the translation to the translation key with an `=` sign, for example, `button.start.openFile = Open`.
