# windows-script-for-generate-the-datetime-file-name
windows script for generate the datetime file name

open notepad

paste these :
```
echo off
set YYYY=%date:~10,4%
set MM=%date:~4,2%
set DD=%date:~7,2%
set HH=%time:~0,2%
if %HH% lss 10 (set HH=0%time:~1,1%)

set NN=%time:~3,2%
set SS=%time:~6,2%
set MS=%time:~9,2%

set FILENAME=%YYYY%%MM%%DD%-%HH%%NN%%SS%
echo "this is log data" > LOG_%FILENAME%.log
```

save as LOG.BAT

you can run with start --> CMD --> LOG.BAT

then output file : LOG_20210407_112300.log

