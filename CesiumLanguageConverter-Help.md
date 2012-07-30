CesiumLanguageConverter is a command line utility that converts various file formats to CZML. 

After building the included `CesiumLanguageConverter` project, the executable can be found in the directory `DotNet/CesiumLanguageConverter/bin/Debug`.

## Usage
`CesiumLanguageConverter [OPTIONS] [FILENAME]`

`FILENAME` can be either a relative or absolute file path.

## Supported file formats
* [[KML]]
* WebGLGlobeJSON.

## Options
* `-h, - ?, --help` 
	* Show this message and exit.

* `-o, --outputFile=VALUE` 
	* Specify the output file name.  Defaults to the  input file name, with extension changed to czml.

* `-t, --type=VALUE` 
	* Specify the type of input file.  By default it will be inferred from the extension of the input file.  Valid options: KML, WebGLGlobeJSON.

* `--pretty`  
	* Produce pretty-printed output, which is more easily readable, but produces larger files.

* `--webGLGlobeJsonHeightScalar=VALUE` 
	 * A scale factor for the height component of each coordinate.  Defaults to 1.

##Examples
* `CesiumLanguageConverter --webGLGlobeJsonHeightScalar=4000000 helloWorld.json` 
* `CesiumLanguageConverter C:\Users\admin\Desktop\sample.kml`
* `CesiumLanguageConverter --pretty -t KML -o stateBorders test.txt`
