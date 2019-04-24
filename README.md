# PowerShell 

## PowerShell for Pentesters

# Table of Contents
1. [Basics](#basics)
2. [Cmdlets](#cmdlets)
    1. [Exploring and Using Cmdlets](#exploring-and-using-cmdlets)
        1. [Get-Command](#get-command)
        2. [Get-Process](#get-process)
        3. [Get-Service](#get-service)
        4. [Start-Process](#start-process)
        5. [Stop-Process](#stop-process)
        6. [Get-HotFix](#get-hotFix)
        7. [Get-Help](#get-help)
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

#### Get-Command

**DESCRIPTION**

The **Get-Command** cmdlet gets all commands that are installed on the computer, including cmdlets, aliases, functions,workflows, filters, scripts, and applications. Get-Command gets the commands from Windows PowerShell modules and snap-ins and commands that were imported from other sessions. To get only commands that have been imported into the current session, use the ListImported parameter.

```Get-Help Get-Command |more```

![Get-Help Get-Command |more](2019-04-23-23-12-39.png)

```Get-Command |more```

![Get-Command |more](2019-04-23-23-24-28.png)

```Get-Command -CommandType Cmdlet |more```

![Get-Command -CommandType Cmdlet |more](2019-04-23-23-26-01.png)

**REMARKS**

To see the examples, type: **"get-help Get-Command -examples"**.
For more information, type: **"get-help Get-Command -detailed"**.
For technical information, type: **"get-help Get-Command -full"**.
For online help, type: **"get-help Get-Command -online"**

```Get-Help Get-Command -full |more```

![Get-Help Get-Command -full |more](2019-04-23-23-29-37.png)

**PARAMETERS**

```Get-Help Get-Command -Parameter * |more```

![Get-Help Get-Command -Parameter * |more](2019-04-23-23-35-23.png)

**Cmdlet Process**

```Get-Command -CommandType Cmdlet -Name *process*```

![Get-Command -CommandType Cmdlet -Name *process*](2019-04-23-23-42-07.png)

**Cmdlet Service**

```Get-Command -CommandType Cmdlet -Name *service*```

![Get-Command -CommandType Cmdlet -Name *service*](2019-04-23-23-43-45.png)

**Measure-Object**

810 Cmdlet Installed

```Get-Command -CommandType Cmdlet |Measure-Object```

![Get-Command -CommandType Cmdlet |Measure-Object](2019-04-23-23-48-21.png)

#### Get-Process

```Get-Process |more```

![Get-Process |more](2019-04-23-23-55-02.png)

#### Get-Service

```Get-Service |more```

![Get-Service |more](2019-04-23-23-56-20.png)

```Get-Command -Verb stop```

![Get-Command -Verb stop](2019-04-23-23-58-42.png)

```Get-Command -Verb start```

![Get-Command -Verb start](2019-04-24-00-01-35.png)

#### Start-Process

```Get-Help Start-Process -Examples |more```

![Get-Help Start-Process -Examples |more](2019-04-24-00-03-22.png)

```Start-Process -FilePath notepad.exe```

![Start-Process -FilePath notepad.exe](2019-04-24-00-11-08.png)

#### Stop-Process

```Stop-Process -Name notepad```

```Get-Process notepad```

![Get-Process notepad](2019-04-24-00-16-08.png)

```Stop-Process -Id 6292```

![Stop-Process -Id 6292](2019-04-24-00-17-41.png)

#### Get-HotFix

```Get-HotFix```

![Get-HotFix](2019-04-24-00-34-03.png)

#### Get-Help

```Get-Help *cmdlets*```

![Get-Help *cmdlets*](2019-04-24-00-41-05.png)

```Get-Help *command*```

![Get-Help *command*](2019-04-24-00-41-56.png)


### Exercises

Explore cmdlets using **Get-Command** and pick ten cmdlets which could be useful in penetration tests.


## Third Example