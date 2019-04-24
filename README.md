# PowerShell 

## PowerShell for Pentesters

# Table of Contents
1. [Basics](#basics)
2. [Cmdlets](#cmdlets)
    1. [Exploring and Using Cmdlets](#exploring-and-using-cmdlets)
    2. [Exercises](#exercises)
3. [Third Example](#third-example)

## Basics

Install **Update-Help** your computer. Enter **Y**

```Get-Help Get-Help -Examples |more```

![Get-Help](2019-04-23-21-49-46.png)


Use **Get-Help** to retrieve help about **Get-Command**:

```Get-Help Get-Command |more```

![Get-Command](2019-04-23-21-24-38.png)

Use **Get-Help about_[topic]** to retrieve help about **powershell.exe**:

```Get-Help powershell```

![Get-Help powershell](2019-04-23-22-02-36.png)

```Get-Help about_PowerShell.exe```

![Get-Help about_PowerShell.exe](2019-04-23-22-03-22.png)

## Cmdlets

### Exploring and Using Cmdlets

**DESCRIPTION**
    The **Get-Command** cmdlet gets all commands that are installed on the computer, including cmdlets, aliases, functions,
    workflows, filters, scripts, and applications. Get-Command gets the commands from Windows PowerShell modules and
    snap-ins and commands that were imported from other sessions. To get only commands that have been imported into the
    current session, use the ListImported parameter.

```Get-Help Get-Command |more```

![Get-Help Get-Command |more](2019-04-23-23-12-39.png)



### Exercises



## Third Example