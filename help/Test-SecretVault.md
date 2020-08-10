---
external help file: Microsoft.PowerShell.SecretManagement.dll-Help.xml
Module Name: Microsoft.PowerShell.SecretManagement
online version:
schema: 2.0.0
---

# Test-SecretVault

## SYNOPSIS
Runs an extension vault self test.

## SYNTAX

```
Test-SecretVault [-Vault] <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet runs an extension vault self test, by running the internal vault 'Test-SecretVault' command.
It will return 'True' if all tests succeeded, and 'False' otherwise.
Information on failing tests will be written to the error stream as error records.

## EXAMPLES

### Example 1
```powershell
PS C:\> Test-SecretVault -Vault CredMan
True
```

This example runs self tests on the 'CredMan' extension vault.
All tests succeeded so no errors are written and 'True' is returned.

## PARAMETERS

### -Vault
Name of vault to run self tests on.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Boolean
## NOTES

## RELATED LINKS
