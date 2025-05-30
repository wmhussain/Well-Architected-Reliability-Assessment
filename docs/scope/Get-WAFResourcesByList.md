---
external help file: scope-help.xml
Module Name: scope
online version:
schema: 2.0.0
---

# Get-WAFResourcesByList

## SYNOPSIS
Filters a list of objects based on resource identifiers.

## SYNTAX

```
Get-WAFResourcesByList [-ObjectList] <Array> [-FilterList] <Array> [-KeyColumn] <String> [-NotIn]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Get-WAFResourcesByList function takes a list of objects and filters them based on the specified resource identifiers.
It compares the KeyColumn property of each object with the provided filter list.

## EXAMPLES

### EXAMPLE 1
```
$objectList = @(
    @{ Id = "/subscriptions/12345/resourceGroups/myResourceGroup/providers/Microsoft.Compute/virtualMachines/myVM" },
    @{ Id = "/subscriptions/12345/resourceGroups/myResourceGroup/providers/Microsoft.Compute/virtualMachines/anotherVM" }
)
$filterList = @("/subscriptions/12345/resourceGroups/myResourceGroup/providers/Microsoft.Compute/virtualMachines/myVM")
```

$filteredObjects = Get-WAFResourcesByList -ObjectList $objectList -FilterList $filterList -KeyColumn "Id"

## PARAMETERS

### -ObjectList
An array of objects to be filtered.

```yaml
Type: Array
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilterList
An array of resource identifiers to filter the objects.

```yaml
Type: Array
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyColumn
The name of the property in the objects that contains the resource identifier.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotIn
{{ Fill NotIn Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
{{ Fill ProgressAction Description }}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
Author: Your Name
Date: 2024-08-07

## RELATED LINKS
