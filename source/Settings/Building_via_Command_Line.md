# Building via Command Line

**NOTE** Building executable packages via command line is only available
on specific licences, so please look at [this
page](https://help.yoyogames.com/hc/en-us/articles/115002637011) to find
out whether your licence supports that. For all other licences, you can
run and debug your project through a command line without any
restrictions. In addition to building your project through the IDE,
GameMaker allows you to build your projects through a command-line
interface using the many options and commands described below. You can
use this to build your project, test it and deploy it to multiple
platforms by running one batch file, and to set up continuous
integration through an automation server such as
[Jenkins](https://www.jenkins.io/) . This is done by running the
Igor.exe executable present within your runtime folder and passing in
the options and commands listed on this page. On Windows this will be
present in the
C:\ProgramData\GameMaker\Cache\runtimes\runtime-\[version\]\bin folder
and on Mac under
/Users/Shared/GameMaker/Cache/runtimes/runtime-\[version\]/bin .

# Igor CI Building

## Setting Up

To set up CI building on a machine, you will need to do the following:

-   Install GameMaker and the runtimes needed
-   Build the projects through the IDE for the targets required, to make
    sure that they work fine
-   Test building from the command line (see examples below)
-   Create a batch file that will do the build that you require within
    the task (test this from the command line)
-   Set up a CI environment (this depends on how you are going to build
    your games); we suggest using [Jenkins](https://www.jenkins.io/)
-   Set up your CI task and ensure that all the prerequisites are setup
    (i.e. source control sync to your project)
-   Hook the batch file into the CI task and test within the Jenkins
    environment

## Notes

-   Some platforms may have issues with the length of your file paths,
    in which case you will need to
    [subst](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/subst)
    virtual drives on your PC (like the IDE does) before passing them
    into your commands
-   Some platforms (notably Android) will automatically subst a drive
    while building, so you may need to manually clean this up in the
    event of an error

## Options

Here are the options that you can use while running the **Igor**
executable:

|                                    |                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Option                             | Description                                                                                                                                                                                                                                                                                                                                                                                            |
|  /uf=\[user_folder\]               | The user folder used for retrieving licence information On Windows, this will be: %appdata%\GameMaker\\\_ On macOS, this will be: \~/.config/GameMaker/\_                                                                                                                                                                                                                                              |
|  /rp=\[runtime_root\]              | The root folder of the runtime                                                                                                                                                                                                                                                                                                                                                                         |
|  /project=\[project_YYP_file\]     | The full path to the project's .yyp file                                                                                                                                                                                                                                                                                                                                                               |
|  /cache=\[cache_dir_path\]         | The cache directory to use (defaults to \cache in the current directory)                                                                                                                                                                                                                                                                                                                               |
|  /temp=\[temp_dir_path\]           | The temporary directory to use (defaults to c:\temp )                                                                                                                                                                                                                                                                                                                                                  |
|  /of=\[output_folder_filename\]    | The output directory where the build will be extracted; do not specify just a directory as the trailing entry is always removed (e.g.: specifying d:\game\output will place the game files in d:\game ) If this is not specified, a directory named output will be created in the same directory as the .bat file (or where the command is running from), containing the extracted build files         |
|  /tf=\[target_file\]               | The actual file name of the ZIP file or NSIS installer that is created                                                                                                                                                                                                                                                                                                                                 |
|  /config=\[configName\]            | The name of the configuration to use (defaults to Default )                                                                                                                                                                                                                                                                                                                                            |
|  /runtime=YYC\|VM                  | The output type (either YYC or VM), defaults to VM                                                                                                                                                                                                                                                                                                                                                     |
|  /j=\[NumCPUs\]                    | The number of CPUs to use during the build process                                                                                                                                                                                                                                                                                                                                                     |
|  /device=\[device_name_from_IDE\]  | The name of the target device as set up in the IDE                                                                                                                                                                                                                                                                                                                                                     |

## Examples

Below you can find examples of build commands for all platforms: [ Opera
GX Opera GX ](#) Cleaning Opera GX project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- OperaGX Clean
```

Running Opera GX:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- OperaGX Run
```

[ Windows Windows ](#) Cleaning Windows project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- Windows Clean
```

Building VM for Windows -- Run , PackageZip and PackageNsis :

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- Windows Run
```

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] -- Windows PackageZip
```

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] -- Windows PackageNsis
```

Building YYC for Windows-- Run , PackageZip and PackageNsis :

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /platform=YYC -- Windows Run
```

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC -- Windows PackageZip
```

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC -- Windows PackageNsis
```

[ macOS macOS ](#) Cleaning macOS project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- Mac Clean
```

Building VM for macOS while on a Mac:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] -- Mac Package
```

**Note** that on Mac you will need to use mono to run Igor, so you will
need to write **mono** before all your commands, e.g.: mono Igor.exe
\[options\] Building VM for macOS while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- Mac Package
```

Building YYC for macOS while on a Mac:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC -- Mac Package
```

Building YYC for macOS while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- Mac Package
```

[ Linux / Ubuntu Linux / Ubuntu ](#) Cleaning Linux project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- Linux Clean
```

Building VM for Linux while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- Linux Package
```

Building YYC for Linux while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- Linux Package
```

[ HTML5 HTML5 ](#) Cleaning HTML5 project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- HTML5 Clean
```

Building HTML5 folder (make sure to specify a target folder with /tf) :

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_folder] -- HTML5 folder
```

[ iOS iOS ](#) Building VM for iOS while on a Mac:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] -- ios Package
```

Building VM for iOS while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- ios Package
```

Building YYC for iOS while on a Mac:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC -- ios Package
```

Building YYC for iOS while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- ios Package
```

[ Android Android ](#) Cleaning Android project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- Windows Clean
```

Building an Android APK using VM:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] -- Android Package
```

Building an Android APK using YYC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC -- Android Package
```

[ tvOS tvOS ](#) Cleaning tvOS project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- tvos Clean
```

Building VM for tvOS while on a Mac:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] -- tvos Package
```

Building VM for tvOS while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- tvos Package
```

Building YYC for tvOS while on a Mac:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC -- tvos Package
```

Building YYC for tvOS while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- tvos Package
```

[ PS4 PS4 ](#) Cleaning PS4 project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- ps4 Clean
```

Building VM for PS4 while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- ps4 Package
```

Building YYC for PS4 while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- ps4 Package
```

[ PS5 PS5 ](#) Cleaning PS5 project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- ps5 Clean
```

Building VM for PS5 while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- ps5 Package
```

Building YYC for PS5 while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- ps5 Package
```

[ Xbox One Xbox One ](#) Cleaning Xbox One project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- XBoxOne Clean
```

Building VM for Xbox One while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- XBoxOne Package
```

Building YYC for Xbox One while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- XBoxOne Package
```

[ Xbox Series X/S Xbox Series X/S ](#) Cleaning Xbox Series X/S project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- XBoxOneSeriesXS Clean
```

Building VM for Xbox Series X/S:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- XBoxOneSeriesXS Package
```

Building YYC for Xbox Series X/S:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- XBoxOneSeriesXS Package
```

[ Switch Switch ](#) Cleaning Switch project:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] -- Switch Clean
```

Building VM for Switch while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /device=[device_IDE_Name] -- Switch Package
```

Building VM for YYC while on a PC:

``` gml
Igor.exe /uf=[user_folder] /rp=[runtime_path] /project=[project_YYP_file] /cache=[cache_dir_path] /temp=[temp_dir_path] /of=[output_folder_filename] /tf=[target_file] /platform=YYC /device=[device_IDE_Name] -- Switch Package
```

# Igor Runtime

Here are the options that can be used with the Igor runtime:

|                        |                                                                                                                 |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Option                 | Description                                                                                                     |
|  /uf=\[user_folder\]   | Set the user folder used for retrieving licence information so GameMaker knows which modules can be installed   |
|  /lf=\[license_file\]  | Set the direct path to a licence file, can be used as an alternative to setting a user folder ( /uf )           |
|  /ru=\[runtime_url\]   | Set the URL to fetch runtime information from (defaults to the stable release)                                  |
|  /rp=\[runtime_root\]  | Set the local runtime install folder to list the installed runtimes or install new runtimes                     |

Here are the commands that can be used with the Igor runtime:

#### Syntax:

``` gml
Igor.exe [command]
```

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Command                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|  Runtime List                         | Lists the runtimes available on a feed (version number, date/time of build)                                                                                                                                                                                                                                                                                                                                                                                                                      |
|  Runtime ListInstalled \[directory\]  | Lists the runtimes available in the current folder ( directory =full path to the folder) You can specify a directory to look in, but if it's not specified it will default to the current directory This also checks whether there is a receipt.json file and a manifest folder inside the directory (making sure that it's actually a runtime)                                                                                                                                                  |
|  Runtime Info \[version\]             | Prints out information about the most recent runtime on the given feed; also needs a licence file to show information regarding the modules available for the user version can either by a string used to search through the feed titles (e.g.: "739" would show information for all builds containing 739 in their version numbers), or it can be all to show information for all feeds It will list the modules with the .zip file names for each module                                       |
|  Runtime Install \[version\]          | Installs the latest runtime from the given feed using the given version as a search filter; if that is not specified, it defaults to the latest version. It will get all the modules that the user has on their licence.                                                                                                                                                                                                                                                                         |
|  Runtime Verify \[folder=.\]          | Calculates the checksums for all the installed files and compares them to the checksums written into the manifest folder . You can specify a folder to check, however if that is not specified it will default to the current directory. This will flag any files where the checksums don't match, files that are missing and files that should not be there. Do note that the manifest files themselves are not verified and a user can alter the manifest files to match the installed ones.   |

# Igor Testing

Here are the options that can be used for testing your builds with Igor:

|                                           |                                                                                                                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Option                                    | Description                                                                                                                                                                                                         |
|  /uf=\[user_folder\]                      | Set the user folder used for retrieving licence information so GameMaker knows which modules can be installed                                                                                                       |
|  /lf=\[license_file\]                     | Set a direct path to a licence file, can be used as an alternative to setting a user folder ( /uf )                                                                                                                 |
|  /df=\[device_file\]                      | Set a direct path to a devices.json file, can be used as an alternative to setting a user folder ( /uf )                                                                                                            |
|  /timeout=\[number_of_seconds_to_wait\]   | The timeout to use for the test in seconds, defaults to 120 seconds; the test will be stopped after this timeout is over and will be marked as failed                                                               |
|  /waittime=\[number_of_seconds_to_wait\]  | Number of seconds to wait in the main loop before declaring the test as passed, defaults to 30 seconds                                                                                                              |
|  /device=\[device_name\]                  | Used to look up the device name in the user folder's devices.json file                                                                                                                                              |
|  /target=\[list_of_targets\]              | Comma-separated list of targets in the PLATFORM\|DEVICE format, e.g.: /target="Windows\|Local,HTML\|Firefox" If you specify **all** , the tests will attempt to run for every device in the devices.json file       |

There is one command that you can use to run tests with Igor:

``` gml
Igor.exe Tests RunTests [test_directory/test_filename]
```

You must specify either a test directory or a test file name.

-   If it's a directory, Igor will look for a file called tests.json in
    the directory
    -   If the file **is not found** , Igor will recursively search for
        .yyz and .yyp files in the directory
        -   Each project found will be built and run on Windows
        -   It will wait till the runner reaches the main loop
            -   The test passes if the runner is still running after the
                wait time
            -   The test fails if the project does not compile within
                the timeout period, or crashes before the wait time is
                over
    -   If a tests.json file **is found** , Igor will run the tests
        described in the file (see example below)
-   Alternatively, you can supply a direct path to a tests.json file
    instead of a directory

# Tests.json File

## Format

The tests.json file must have the following format:

-   The JSON file should contain an array of objects
-   Each object should describe one test
    -   The test object must contain these keys:
        -    name : A name used to report whether the test has passed or
            failed
        -    path : A path to a .yyp , .yyz , .gml , .js file or folder
            for the test
        -    command : The Igor command for the test ( Run ,
            CreatePackage , etc. as described above)
    -   The test object may also contain these keys:
        -    platform : Passed directly through to Igor to do the test
        -    device : The device name from the devices.json file
        -    target : The target in a " PLATFORM\|TARGET" format, e.g.:
            " Windows\|Local"
        -    timeout : A timeout for the total test including compile
            and run; if exceeded the test will be stopped and marked as
            failed
        -    waittime : The length of time to wait after entering the
            main loop before deciding whether the test has passed
        -    owner : the e-mail address of the user who will be e-mailed
            if this test fails

## Example

Here is an example of a tests.json file:

``` gml
[
  
  {
  
  "name" : "Game Idea Windows",
  
  "path" : "C:/scratch/GameIdea.yyz",
  
  "platform" : "Windows",
  
  "command" : "Run",
  
  "timeout" : "500",
  
  "waittime" : "30"
  
  },
  
  {
  
  "name" : "Platformer Game Windows",
  
  "path" : "C:/Users/&amp;lt;MY USERNAME&amp;gt;/Documents/GameMaker/Platformer Game/PlatformerGame.yyp",
  
  "target" : "Windows|Local,HTML5|selenium:firefox,PS4|Default",
  
  "command" : "Run"
  
  },
  
  {
  
  "name" : "Puzzle Game Windows",
  
  "path" : "C:/Users/&amp;lt;MY USERNAME&amp;gt;/Documents/GameMaker/Puzzle Game/PuzzleGame.yyp",
  
  "platform" : "HTML5",
  
  "command" : "Run",
  
  "device" : "selenium:chrome"
  
  }
  
  ]
```
