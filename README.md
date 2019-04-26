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
        1. [Get-ComputerInfo](#get-computerinfo)
        2. [Get-Content](#get-content)
        3. [Get-History](#get-history)
        4. [Get-PSDrive](#get-psdrive)
        5. [Get-LocalGroup](#get-localgroup)
        6. [Clear-History](#clear-history)
        7. [Invoke-Command](#invoke-command)
        8. [Import-Module](#import-module)
        9. [Get-DnsClient](#get-dnsclient)
        10. [Get-NetRoute](#get-netroute)
3. [Output Formatting](#OutputFormatting)
    1. [Formatting](#formatting)
        1. [Format-Table](#format-table)
        2. [Format-List](#format-list)
    2. [Output Manipulation](#output-manipulation)
        1. [Out-GridView](#out-gridview)
        2. [Out-File](#out-file)
4. [Operators](#operators)
    1. [Arithmetic](#Arithmetic)
    2. [Assignment](#assignment)
    3. [Comparison](#comparison)
    4. [Redirection](#redirection)
    6. [Exercise3](#exercise3)
        1. [Static member operator](#static-member-operator)
        2. [split](#split)
5. [Advanced Operators](#advanced-Operators)
    1. [Logical](#logical)
        1. [-and](#-and)
        2. [-or](#-or)
        3. [-xor](#-xor)
        4. [-not](#-not)
        5. [Negates](#negates)
    2. [Split and Join](#split-and-join)
        1. [-split](#-split)
        2. [-join](#-join)
    3. [Type-Operations](#type-operations)
        1. [-is](#-is)
        2. [-isnot](#-isnot)
        3. [-as](#-as)
6. [Types](#types)
    1. [Get-Type](#get-type)
7. [Arrays](#arrays)
    1. [Type Conversion](#type-conversion)
    2. [Array](#Array)
8. [Conditional Statements](#conditional-statements)
    1. [if elseif else](#if-elseif-else)
    2. [Switch Statement](#switch-statement)
    3. [Switch -Wildcard](#switch--Wildcard)
    4. [Switch -Regex](#switch--Regex)
9. [Loop Statements](#Loop-Statements)
    1. [while](#while)
    2. [foreach](#foreach)
    3. [Loop Cmdlets](loopcmdlets)
        1. [ForEach-Object](#ForEach-Object)
        2. [Where-Object](#Where-Object)
    4. [Exercise4](#Exercise4)
10. [Basic Scripting](#BasicScripting)



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

#### Get-ComputerInfo

```Get-ComputerInfo```

![Get-ComputerInfo](2019-04-24-03-03-13.png)

#### Get-Content

```Get-Content .\log.txt.txt -TotalCount 5 |Set-Content output.txt```

![Get-Content](2019-04-24-03-33-08.png)

#### Get-History

```Get-History |more```

![Get-History](2019-04-24-03-38-27.png)

#### Get-PSDrive

```Get-PSDrive```

![Get-PSDrive](2019-04-24-03-42-20.png)

#### Get-LocalGroup

```Get-LocalGroup```

![Get-LocalGroup](2019-04-24-03-48-27.png)

#### Clear-History

```Clear-History```

![Clear-History](2019-04-24-03-55-58.png)

#### Invoke-Command

```Get-Help Invoke-Command -Examples |more```

![Invoke-Command](2019-04-24-03-58-32.png)

#### Import-Module

```Get-Help Import-Module -Examples |more```

![Import-Module](2019-04-24-04-01-02.png)

#### Get-DnsClient

```Get-Command -Module DnsClient * |more```

![Get-DnsClient](2019-04-24-04-04-15.png)

#### Get-NetRoute

``` Get-Command -Module NetTCPIP |more```

![Get-NetRoute](2019-04-24-04-08-49.png)

## Output Formatting

### Formatting

```Get-Command -CommandType Cmdlet -Name format*```

![Output Formatting](2019-04-25-00-44-32.png)

#### Format-Table

```Get-ChildItem |Format-Table```

![Format-Table](2019-04-25-00-48-37.png)

```Get-ChildItem |Format-Table Name```

![Get-ChildItem |Format-Table Name](2019-04-25-00-54-48.png)

#### Format-List

![Format-List](2019-04-25-01-02-32.png)

### Output Manipulation

```Get-Command -CommandType Cmdlet -Name out*```

![Get-Command -CommandType Cmdlet -Name out*](2019-04-25-01-12-39.png)

#### Out-GridView

```Get-Process |Out-GridView```

![Get-Process |Out-GridView](2019-04-25-01-15-24.png)

#### Out-File

```Get-Process |Out-File -FilePath get_process.txt```

![Get-Process |Out-File -FilePath get_process.txt](2019-04-25-01-26-59.png)

```Get-Content .\get_process.txt |more```

![Get-Content .\get_process.txt |more](2019-04-25-01-28-15.png)

```Get-ChildItem |Format-List * |Out-File -FilePath 'C:\Users\anake\Downloads\list.txt'```

![Get-ChildItem |Format-List * |Out-File](2019-04-25-01-35-14.png)

## Operators

### Arithmetic

## +  ,  -  ,  *  ,  /  ,  % 

![Arithmetic](2019-04-25-02-31-41.png)

### Assignment

## =  ,  +=  ,  -=  ,  *=  ,  /=  ,  %=

![Assignment](2019-04-25-02-34-46.png)

### Comparison

## -eq  ,  -ne  ,  -gt  ,  -lt  ,  -le  ,  -ge  ,  -match  ,  -notmatch  ,  -replace  ,  -like  ,  -notlike  ,  -in  ,  -notin  ,  -contains  ,  -notcontains

![Comparison](2019-04-25-02-56-41.png)

### Redirection

## >  ,  >>  ,  2> , 2>&1

```>```

![Redirection](2019-04-25-03-00-26.png)

```>>```

![Redirection2](2019-04-25-03-01-57.png)

```2>&1```

![Redirection3](2019-04-25-03-06-04.png)

### Exercise3

Explore the PowerShell help system and locate help topics for various operators.

```Get-Help Arith |more```

![Get-Help Arith |more](2019-04-25-03-15-12.png)

SEE ALSO

*about_Arithmetic_Operators*

*about_Assignment_Operators*

*about_Comparison_Operators*

*about_Logical_Operators*

*about_Type_Operators*

*about_Split*

*about_Join*

*about_Redirection*

#### Static member operator

Calls the static properties operator and methods of a .NET Framework class. To find the static properties and methods of an object, use the Static parameter of the Get-Member cmdlet.

```[datetime]::now```

![datetime](2019-04-25-03-20-48.png)

#### split

```$i = 1```

```$c -split {if ($i -lt 1) {$_ -eq ","} else {$_ -eq ";"}}```

![split](2019-04-25-03-54-37.png)



## Advanced Operators

### Logical

#### -and

```Get-Help about_Comparison -Examples |more```

```Get-Help about_Logical -Examples |more```

![-and](2019-04-25-20-03-21.png)

#### -or

![-or](2019-04-25-20-14-19.png)

#### -xor 

![-xor](2019-04-25-20-18-11.png)

#### -not

![-not](2019-04-25-20-24-34.png)

#### Negates

![Negates](2019-04-25-20-27-09.png)


### Split and Join

#### -split

![-split](2019-04-25-20-59-45.png)

#### -join

![-join](2019-04-25-21-02-22.png)

### Type-Operations

#### -is

![-is](2019-04-25-21-05-50.png)

#### -isnot

![-isnot](2019-04-25-21-36-34.png)

#### -as

![-as](2019-04-25-21-41-15.png)

## Types

### Get-Type

PSObject and the Adapted and Extended Type Systems (ATS and ETS) [https://blogs.msdn.microsoft.com/besidethepoint/2011/11/22/psobject-and-the-adapted-and-extended-type-systems-ats-and-ets/][types]


![Get-Type](2019-04-26-01-54-00.png)

![strings](2019-04-26-02-05-11.png)

![strings1](2019-04-26-02-06-43.png)

![strings2](2019-04-26-02-09-25.png)

## Arrays

### Type Conversion

![Type Conversion](2019-04-26-02-19-13.png)

![conv](2019-04-26-02-21-41.png)

### Array

Commands in PowerShell return an array of Objects - **Object[]**

![array](2019-04-26-02-27-12.png)

Index

![array2](2019-04-26-02-29-34.png)

More than one type of elements could be stored.

![empty](2019-04-26-02-31-39.png)

## Conditional Statements

### if elseif else

![if elseif else](2019-04-26-02-42-56.png)

### Switch Statement

![Switch Statement](2019-04-26-02-48-01.png)

### Switch -Wildcard

![switch -Wildcard](2019-04-26-02-58-50.png)

### Switch -Regex

```Get-WindowsUpdateLog```

![Get-WindowsUpdateLog](2019-04-26-03-11-17.png)

```Switch -Regex -File C:\Users\anake\OneDrive\Desktop\WindowsUpdate.log { 'Validating'{$_}}```

![Switch -Regex -File](2019-04-26-03-11-54.png)

## Loop Statements

### while

![while](2019-04-26-03-37-53.png)

### foreach

![foreach](2019-04-26-03-42-25.png)

### Loop Cmdlets

#### ForEach-Object

![ForEach-Object](2019-04-26-03-47-09.png)

#### Where-Object

```Get-ChildItem |Where-Object {$_.Name -match "txt"}```

![Where-Object](2019-04-26-03-51-36.png)

### Exercise4

Iterate through the process running on your computer and print the path of the executable for each process.

``` Get-Process |ForEach-Object -MemberName Path```

![Get-Process |ForEach-Object -MemberName Path](2019-04-26-03-59-10.png)

## Basic Scripting

[types]:    https://blogs.msdn.microsoft.com/besidethepoint/2011/11/22/psobject-and-the-adapted-and-extended-type-systems-ats-and-ets/

