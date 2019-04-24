# PowerShell 

## PowerShell for Pentesters

# Table of Contents
1. [Basics](#basics)
    1. [PowerShell-Basic](#powerShell-basic)
        1. [cd](#cd)
        2. [dir](#dir)
        3. [ls](#ls)
        4. [ps](#ps)
        5. [Get-Help](#get-help)
        6. [Update-Help](#update-help)
        7. [Wildcard](#wildcard)
    2. [Exercises](#exercises1)
2. [Cmdlets](#cmdlets)
    1. [Exploring and Using Cmdlets](#exploring-and-using-cmdlets)
        1. [Get-Command](#get-command)
        2. [Get-Process](#get-process)
        3. [Get-Service](#get-service)
        4. [Start-Process](#start-process)
        5. [Stop-Process](#stop-process)
        6. [Get-HotFix](#get-hotFix)
        7. [Get-Help_](#get-help_)
    2. [Exercises2](#exercises2)

## Basics

### PowerShell-Basic

#### cd 

``` cd \```

![cd](2019-04-24-01-12-40.png)

#### dir

```dir```

![dir](2019-04-24-01-13-12.png)

#### ls

```ls```

![ls](2019-04-24-01-02-25.png)

#### ps

```ps```

![ps](2019-04-24-01-04-30.png)

#### Get-Help

```Get-Help |more```

![`Get-Help |more](2019-04-24-01-16-37.png)

#### Update-Help

Install **Update-Help** your computer. Enter **Y**

```Get-Help Get-Help -Examples |more```

![Get-Help](2019-04-23-21-49-46.png)

#### Wildcard

```Get-Help * |more```

![Get-Help * |more](2019-04-24-01-21-29.png)

```Get-Help *process```

![Get-Help *process](2019-04-24-01-22-55.png)

```Get-Process```

![Get-Process](2019-04-24-01-24-23.png)

```Get-Help *alias*```

![Get-Help *alias*](2019-04-24-01-25-45.png)

```Get-Alias```

![Get-Alias](2019-04-24-01-26-50.png)

```Get-Help Get-Help -Examples |more```

![Get-Help Get-Help -Examples |more](2019-04-24-01-28-00.png)

```Get-Help about_Aliases |more```

![Get-Help about_Aliases |more](2019-04-24-01-29-26.png)

### Exercises

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

#### Get-Help_

```Get-Help *cmdlets*```

![Get-Help *cmdlets*](2019-04-24-00-41-05.png)

```Get-Help *command*```

![Get-Help *command*](2019-04-24-00-41-56.png)

```Get-Help about_Core_Commands |more```

![Get-Help about_Core_Commands |more](2019-04-24-00-47-52.png)

### Exercises2

Explore cmdlets using **Get-Command** and pick ten cmdlets which could be useful in penetration tests.

