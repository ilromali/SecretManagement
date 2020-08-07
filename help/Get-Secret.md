---
external help file: Microsoft.PowerShell.SecretManagement.dll-Help.xml
Module Name: Microsoft.PowerShell.SecretManagement
online version:
schema: 2.0.0
---

# Get-Secret

## SYNOPSIS
Finds and returns a secret by name from registered vaults.

## SYNTAX

```
Get-Secret [-Name] <String> [[-Vault] <String>] [-AsPlainText] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet finds and returns the first secret that matches the provided name.
If a vault name is specified, then only that vault will be searched.
Otherwise, all vaults are searched and the first found result is returned.
If a 'Default' vault is specified, then that vault is searched before any other registered vault.
Secrets that are string or SecureString types are returned as SecureString objects by default.
Unless the '-AsPlainText' parameter switch is used, in which case the secret is returned as a String type in plain text.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-Secret -Name Secret1 -Vault CredMan
System.Security.SecureString

PS C:\> Get-Secret -Name Secret1 -Vault CredMan -AsPlainText
PlainTextSecretString
```

This example searches for a secret with the name 'Secret1', which is a String type secret.
The first time returns the secret as a SecureString object.
The second time uses the '-AsPlainText' and so the secret string is returned as a string object, and is displayed in plain text.

## PARAMETERS

### -AsPlainText
Switch parameter that when used returns either a string or SecureString secret type as a String type (in plain text).
If the secret being retrieved is not of string or SecureString type, this switch parameter has no effect.

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

### -Name
Name of the secret to be retrieved.
Wild card characters are not allowed.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Vault
Optional name of the registered vault to retrieve the secret from.
If no vault name is specified, then all registered vaults are searched.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
