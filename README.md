# Runner

# Requirement

- python 3
- python-psutil

# Initialize linux environment

Ubuntu:

``` txt
sudo apt-get install python3 python3-psutil -y
cp runner /usr/bin
chmod +x /usr/bin/runner
```

# Build windows executable

Download and install:

- python 3.5 from https://www.python.org/downloads
- psutil from https://pypi.python.org/pypi/psutil
- pywin32 from https://sourceforge.net/projects/pywin32/files/pywin32

Install pyinstaller:

``` txt
%LOCALAPPDATA%\Programs\Python\Python35-32\Scripts\pip.exe install pyinstaller
```

Generate windows executable:

``` txt
%LOCALAPPDATA%\Programs\Python\Python35-32\Scripts\pyinstaller.exe -c -F runner
```

# Usage

``` txt
Input:
	First Line: user_time_limit_in_milliseconds [total_time_limit_in_milliseconds]
	Second Line: command_line
	stdin.txt (optional)
Output:
	stdout.txt
	stderr.txt
	runner.json
```

runner.json example:

``` txt
{
	"Error": "",
	"Command": "sleep 1",
	"IsTimeout": false,
	"UserTime": 0,
	"TotalTime": 1018,
	"PeakMemory": 770048,
	"ExitCode": 0
}
```

TODO: runner.exe is not updated
