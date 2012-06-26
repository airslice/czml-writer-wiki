## Get the Code

* `git clone git@github.com:AnalyticalGraphicsInc/czml-writer.git`
	* Or download the [zip](https://github.com/AnalyticalGraphicsInc/czml-writer/zipball/master)

## .NET

Using Visual Studio 2010, Express, or newer on Windows:
* Open `DotNet\CesiumLanguageWriter.sln`
* Build the solution:  Build - Build Solution (Ctrl + Shift + B)
* Open one of the included test projects using [Nunit](http://www.nunit.org/) to run unit tests. See the [Contributor's Guide](https://github.com/AnalyticalGraphicsInc/czml-writer/wiki/Contributor's-Guide#wiki-NUnit) for NUnit setup and usage instructions. 

Using [MonoDevelop](http://monodevelop.com/) on Linux or Mac:
* Open `DotNet\CesiumLanguageWriter.sln`
* Build the included projects:  Build - Build All (F8)
* Running unit tests:  Choose a test project or file from the solution view and select Run - Run Unit Tests (Ctrl + T)

##Java:

* In [Eclipse](http://www.eclipse.org/):
	* File - Import - General - Existing Projects into Workspace
	* Select root directory: `\czml-writer\Java`
* Build the included projects:
	* Project - Build All (Ctrl + B)
	* Or select Project - Build Automatically to build when changes are saved.
* Run the unit tests:
	* In the Package or Project Explorer (Window - Show View), right-click the test project or file and select Run-As - [Junit](http://www.junit.org/) Test