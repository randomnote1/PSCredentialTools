---
external help file:
Module Name: PSCredentialTools
online version:
schema: 2.0.0
---

# ConvertFrom-PKISecureString

## SYNOPSIS

Converts a SecureString object into encrypted text with the public key of a PKI certificate.

## SYNTAX

### CertFile

```PowerShell
ConvertFrom-PKISecureString [-SecureString] <SecureString> -CertificateFile <String> [<CommonParameters>]
```

### Thumbprint

```PowerShell
ConvertFrom-PKISecureString [-SecureString] <SecureString> -Thumbprint <String> [-CertificateStore <String>]
 [<CommonParameters>]
```

## EXAMPLES

### EXAMPLE 1

Encrypts a SecureString object and saves it to disk.

```PowerShell
ConvertFrom-PKISecureString -SecureString $MySecretValue -Thumbprint '87BB70A19A7671D389F49AF4C9608B2F381FDD80' | Out-File ./encryptedText.txt
```

## PARAMETERS

### -SecureString

The SecureString object that will returned as an encrypted string.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Thumbprint

The ThumbPrint of a certificate on the local computer that will be used to encrypt the string.

```yaml
Type: String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFile

Path to a .CER certificate public key file that will be used to encrypt the string.

```yaml
Type: String
Parameter Sets: CertFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateStore

Specifies the certifcate store of the specified certificate thumbprint.
Either LocalMachine or CurrentUser.

```yaml
Type: String
Parameter Sets: Thumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters ([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)).
