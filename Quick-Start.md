## Binaries

#### .NET

Binary releases are [available on NuGet](https://www.nuget.org/packages/CesiumLanguageWriter/), or on the [releases page](https://github.com/AnalyticalGraphicsInc/czml-writer/releases).

#### Java

Binary releases are available for download on the [releases page](https://github.com/AnalyticalGraphicsInc/czml-writer/releases).

## Building from source 

#### .NET

Using Visual Studio 2019 on Windows:
* Open `DotNet\CesiumLanguageWriter.sln`
* Build the solution:  Build - Build Solution (Ctrl + Shift + B)
* Open one of the included test projects using [NUnit](http://www.nunit.org/) to run unit tests. See the [Contributor's Guide](https://github.com/AnalyticalGraphicsInc/czml-writer/wiki/Contributor's-Guide#wiki-NUnit) for NUnit setup and usage instructions. 

#### Java:

* In [IntelliJ IDEA](https://www.jetbrains.com/idea/):
  * File - Import - General - Existing Projects into Workspace
  * Open the project using directory: `\czml-writer\Java`
* Build the projects:
  * Build - Build Project
* Run the unit tests:
  * In the Project view, right-click the `CesiumLanguageWriterTests` project and select Run 'All Tests'.

Or using [Gradle](https://gradle.org/):
  * `gradlew build`