---
applicable: SharePoint Online
external help file: PnP.PowerShell.dll-Help.xml
Module Name: PnP.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnpplannertask
schema: 2.0.0
title: get-pnpplannertask
---

# Get-PnPPlannerTask

## SYNOPSIS
Returns Planner tasks

## SYNTAX

### By Group
```powershell
Get-PnPPlannerTask -Group <PlannerGroupPipeBind> -Plan <PlannerPlanPipeBind> [-ResolveUserDisplayNames]
 [-ByPassPermissionCheck] [<CommonParameters>]
```

### By Bucket
```powershell
Get-PnPPlannerTask -Bucket <PlannerBucketPipeBind> [-ResolveUserDisplayNames] [-ByPassPermissionCheck]
 [<CommonParameters>]
```

### By Plan Id
```powershell
Get-PnPPlannerTask -PlanId <String> [-ResolveUserDisplayNames] [-ByPassPermissionCheck] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet returns Planner tasks.

## EXAMPLES

### Example 1
```powershell
Get-PnPPlannerTask -Group "Marketing" -Plan "Conference Plan"
```

This returns all tasks for the specific plan.

### Example 2
```powershell
$tasks = Get-PnPPlannerTask -Group "Marketing" -Plan "Conference Plan" -ResolveUserDiplayNames
$task = $tasks | Select-Object -First 1
$task.CreatedBy.DisplayName 
```

This retrieves all tasks for a specific plan, takes the first task and prints the display name of the user that created the task.

### Example 3
```powershell
Get-PnPPlannerTask -Group "Marketing" -PlanId "QvfkTd1mc02gwxHjHC_43JYABhAy"
```

This returns all tasks for the specified plan.

## PARAMETERS

### -Bucket
Specify the bucket or bucket id to retrieve the tasks for.

```yaml
Type: PlannerBucketPipeBind
Parameter Sets: By Bucket
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Group
Specify the group id of group owning the plan.

```yaml
Type: PlannerGroupPipeBind
Parameter Sets: By Group
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan
Specify the id or name of the plan to retrieve the tasks for.

```yaml
Type: PlannerPlanPipeBind
Parameter Sets: By Group
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanId
Specify the id of the plan to retrieve the tasks for.

```yaml
Type: String
Parameter Sets: By Plan Id
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResolveUserDisplayNames
{{ Fill ResolveUserDisplayNames Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Microsoft 365 Patterns and Practices](https://aka.ms/m365pnp)
