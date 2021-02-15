# PyCompressedCracker
Bruteforce attack for Compressed file using 7z

If there is no 7z installed in your computer , you can get an instance at [7z](https://www.7-zip.org/) , and you need to make sure

that 7z can run using command line .Typically if you are using windows ,you can simply your 7z to a dictionary and then run it in command line.

If you are using  unrar ,you can goto [PyRarCrack](https://github.com/dunossauro/PyRarCrack) for more help.



### useage:

```
usage: pyrarcrack.py [-h] [--start START] [--stop STOP] [--verbose VERBOSE] [--alphabet ALPHABET] [--file FILE]

Python combination generator to decompress

optional arguments:
  -h, --help           show this help message and exit
  --start START        Number of characters of the initial string [1 -> "a", 2 -> "aa"]
  --stop STOP          Number of characters of the final string [3 -> "ßßß"]
  --verbose VERBOSE    Show combintations
  --alphabet ALPHABET  alternative chars to combinations
  --file FILE          Compressed file [fileName]
```

### Example

Files:

```txt
2021/02/03  01:34             8,194 1.rar            <-- the target
2019/02/20  19:00           108,074 7-zip.chm
2019/02/22  00:00            78,336 7-zip.dll
2019/02/22  00:00            50,688 7-zip32.dll
2019/02/22  00:00         1,679,360 7z.dll
2019/02/22  00:00           468,992 7z.exe
2019/02/22  00:00           205,824 7z.sfx
2019/02/22  00:00           186,880 7zCon.sfx
2019/02/22  00:00           867,840 7zFM.exe
2019/02/22  00:00           581,632 7zG.exe
2018/01/28  17:00               366 descript.ion
2019/02/22  17:26            48,844 History.txt
2021/02/11  22:16    <DIR>          Lang
2019/01/09  18:15             3,990 License.txt
2021/02/11  15:08             2,551 pyrarcrack.py    <-- the py file 
2021/02/11  22:28               842 README.md
2019/02/22  17:28             1,688 readme.txt
2019/02/22  01:00            15,360 Uninstall.exe
```

CommandLine:

```
python pyrarcrack.py --start 4 --stop 10 --file 1.rar --alphabet 0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ --verbose True

Password found: 1234567890
Time: 95816.41711735725
```
