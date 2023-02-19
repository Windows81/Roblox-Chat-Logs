<h2 align="center"> Revel in the fact that I log most of my interactions on Rōblox! </h2>

**Download the repository [as a zipped file](https://github.com/Windows81/Roblox-Chat-Logs/archive/refs/heads/main.zip) if you don't know how else to parse the entire chatlog archive.** You can navigate the file heirarchy in its most recent state through the following sequences of Bash commands.

```bash
curl https://github.com/Windows81/Roblox-Chat-Logs/archive/refs/heads/main.zip -Ls --output temp.zip
unzip -l temp.zip "*/*.txt" | head - -n -2 | tail - -n +5 | cut -c 53- | less
rm temp.zip
```

You can modify the second line to pipe the result of this command to filter further.
To pipe and sort the results by date:

```bash
curl https://github.com/Windows81/Roblox-Chat-Logs/archive/refs/heads/main.zip -Ls --output temp.zip
unzip -l temp.zip "*/*.txt" | head - -n -2 | tail - -n +5 | cut -c 53- | sort -k 1.13 | less
rm temp.zip
```

To read the contents of a single file:

```bash
n="12370619045 2023-02-15 021232.txt"
curl https://github.com/Windows81/Roblox-Chat-Logs/archive/refs/heads/main.zip -Ls --output temp.zip
unzip -p temp.zip "*/$n" | less
rm temp.zip
```
