## Wednesday, March 24, 2021, 1:58:42PM EDT <1616608722>

TIL how to add `vi` history mode to (ugh) PowerShell:

```
Get-Module -Name PSReadline -ListAvailable
Find-Package -Name PSReadlineGet-Module -Name PSReadline -ListAvailable
Install-Package -Name PSReadline -Force
Set-PSReadlineOption -EditMode vi -BellStyle None
```

And to download Vim:

```
Invoke-WebRequest -Uri https://ftp.nluug.nl/pub/vim/pc/gvim80-586.exe `
  -Outfile ~\Downloads\gvim80-586.exe
# (install vim by running exe)
New-Alias -Name vi -Value 'C:\Program Files (x86)\vim\vim80\vim.exe'
New-Alias -Name vim -Value 'C:\Program Files (x86)\vim\vim80\vim.exe'
```

<https://codeandkeep.com/PowerShell-And-Vim/>

## Wednesday, March 24, 2021, 12:18:12PM EDT <1616602692>

TIL that POSIX shell does not allow `IFS= while ...` and the `IFS=` must
be on its own line.

## Wednesday, March 24, 2021, 11:37:41AM EDT <1616600261>

Need to learn about Dask, an "alternative" to Apache Spark. People are
gaga for it, but it mostly looks very marketing driven and pretty sucky.

## Wednesday, March 24, 2021, 10:35:21AM EDT <1616596521>

Time to stop calling learning projects *challenges* and to start calling
them *labs*, which is what they are, an opportunity to change lots of
variables and experiment rather than just pass the challenge. In fact,
this discovery has made me view the word "challenge" pejoratively
forever more. A challenge is something to be met and completed giving
you fame and glory. A lab is something to be done methodically,
experimentally, and with the astute attention of a scrupulous engineer
or scientist. Labs can be done several times and each time something new
can be discovered, learned, and eventually mastered. Repetition *is* the
mother of learning and people don't tend to repeat a "challenge." They
just finish it and get it out of the way.

Words matter, and this discovery really makes me happy.

## Wednesday, March 24, 2021, 3:20:28AM EDT <1616570428>

Here's the book we *really* need:

*Learning Idiomatic Go in the Linux Terminal*

*That* is what is needed, not this shit that assumes "VSCode or Goland"
written by Mac dweebs.

