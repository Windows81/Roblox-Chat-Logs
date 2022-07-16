<h2 align="center"> Revel in the fact that I log most of my interactions on Rōblox! </h2>

In the case more than 1000 files happen to exist here, you can get the URLs of all of them through the following command line. You can pipe the result of this command to filter further.

```bash
curl -s "https://api.github.com/repos/Windows81/Roblox-Chat-Logs/contents?ref=main"|grep -Po "(?<=html_url....).+\.txt"
```

To pipe and sort the results by date:

```bash
|sort -k 1.91
```
