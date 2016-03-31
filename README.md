# CloudStartupScriptWrapper
This is a python program designed for running startup/shutdown scripts on a compute instance. It is particularly useful for logging outputs of multiple commands as well as logging system cpu, memory, and i/o usage. 

## Dependencies
* optparse
* psutil

## Usage

python Startup.py --S 'commands to run separated by \n' --H 'HistoryFile' --N 'name' --SD 'onShutdown' --PF 'performanceDataFile'

|Option | Description|
|--- | ---|
|S | This should be the text of commands to run separated by \n.|
|H | The path and name of a file to save command history. This will be in pickle format.|
|N | The name of the instance that is running.|
|SD | Commands to run on shutdown.|
|PF | The path and name of a file to save performance data in TSV format.|

## Example

python Startup.py --S 'echo hello\necho world' --H ./history.pickle --N instance1 --SD 'echo goodbye' --PF performance.tsv
