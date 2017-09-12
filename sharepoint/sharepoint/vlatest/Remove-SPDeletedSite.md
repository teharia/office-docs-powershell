---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Remove-SPDeletedSite

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Remove-SPDeletedSite [-Identity] <SPDeletedSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-ContentDatabase <SPContentDatabasePipeBind>] [-WebApplication <SPWebApplicationPipeBind>]
 [-WhatIf]
```

## DESCRIPTION
This cmdlet was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).

Use the Remove-SPDeletedSite cmdlet to permanently remove a deleted site collection from the farm.

Unlike the Remove-SPSite cmdlet that uses the host name and scheme for the Identity parameter (that is, http://server_name), the value of the identity parameter for all SPDeletedSite cmdlets use a server-relative URL.
Typically, the forward slash character (/) begins the relative URL and also denotes the root site.

For additional information about a server-relative URL or understanding general concepts about absolute and relative URLs, see Server Relative URL Property (http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.spsite.serverrelativeurl.aspx) or Understanding Absolute and Relative URL Addresses (http://msdn.microsoft.com/en-us/library/bb208688(office.12).aspx).

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE----------------------- (SharePoint Server 2013)
```
C:\PS>Remove-SPDeletedSite -Identity 610857cb-8414-4a89-8bf3-ad3628f6c86c
```

This example permanently removes a specific deleted site collection by using a site ID.

### ------------------EXAMPLE----------------------- (SharePoint Server 2016)
```
C:\PS>Remove-SPDeletedSite -Identity 610857cb-8414-4a89-8bf3-ad3628f6c86c
```

This example permanently removes a specific deleted site collection by using a site ID.

## PARAMETERS

### -Identity
Specifies the identity of the deleted site collection to permanently delete.
The identity can be either a valid server-relative URL in the form /sites/site_name; a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an SPDeletedSite object.

```yaml
Type: SPDeletedSitePipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentDatabase
Specifies the GUID of the content database from which to list site collections.

The type must be a valid database name in the form SPContentDB01 or a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebApplication
Specifies the URL, GUID, or name of the Web application from which to list sites.

The type must be a valid URL in the form http://server_name; a valid GUID, for example, 12345678-90ab-cdef-1234-567890bcdefgh; or the Web application name, for example, WebApplication1212.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WhatIf
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
