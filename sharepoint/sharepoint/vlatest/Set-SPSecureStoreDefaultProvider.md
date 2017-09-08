---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Set-SPSecureStoreDefaultProvider

## SYNOPSIS
Updates the secure store provider.

## SYNTAX

```
Set-SPSecureStoreDefaultProvider -Type <Type> [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
The Set-SPSecureStoreDefaultProvider cmdlet sets or replaces the secure store provider.
To register a third-party secure store, implement the ISecureStoreProvider interface.
With the interface defined, place the DLL file in the global assembly cache, and then load the DLL and load the type, as shown in the example.
You can then set the secure store provider.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
C:\PS>[Reflection.Assembly]::LoadFrom("C:\ContosoFolder\contosoSecureStore.dll")

C:\PS>$type = [Contoso.SecureStore.ContosoSecureStoreProvider]

C:\PS>Set-SPSecureStoreDefaultProvider -Type $type
```

This example sets the custom implemented secure store provider.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>[Reflection.Assembly]::LoadFrom("C:\ContosoFolder\contosoSecureStore.dll")

C:\PS>$type = [Contoso.SecureStore.ContosoSecureStoreProvider]

C:\PS>Set-SPSecureStoreDefaultProvider -Type $type
```

This example sets the custom implemented secure store provider.

## PARAMETERS

### -Type
The type must be a secure store provider type enclosed in square brackets; for example, \[Reflection.Assembly\].

```yaml
Type: Type
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
