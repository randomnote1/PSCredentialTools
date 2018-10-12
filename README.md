# PSCredentialTools

PSCredentialTools provides methods for securly generating, storing and retrieving credentials and other sensitive data for use in PowerShell scripts and Desired State Configurations. Credentials can be saved to disk, encrypted with either a pre-shared-key or with a PKI certificate. Credentials can also be stored in Azure KeyVault as an Azure KeyVault Secret.

## Branches

### dev

This is the development branch to which contributions should be proposed by contributors as pull requests. This development branch will periodically be merged to the master branch, and be released to [PowerShell Gallery](https://www.powershellgallery.com/).

## Installation

### From GitHub source code

To manually install the module, download the source code from GitHub and unzip the contents to the `$env:ProgramFiles\WindowsPowerShell\Modules` folder.

### From PowerShell Gallery

To install from the PowerShell gallery using PowerShellGet run the following command:

```powershell
Find-Module -Name PSCredentialTools | Install-Module
```

To confirm installation, run the following command to ensure the PSCredentialTools commands are available.

```powershell
Get-Command -Module PSCredentialTools
```

## Commands

- [**ConvertFrom-FIPSSecureString**](.\docs\ConvertFrom-FIPSSecureString.md) converts a PowerShell SecureString object into encypted text, using a pre-shared-key. It uses the FIPS compliant AES Crypto Provider.
- [**ConvertFrom-PKISecureString**](.\docs\ConvertFrom-PKISecureString.md) converts a PowerShell SecureString object into encrypted text using a provided certificate's Public Key.
- [**ConvertTo-FIPSSecureString**](.\docs\ConvertTo-FIPSSecureString.md) converts a previously encrypted SecureString with a pre-shared-key back into a PowerShell SecureString object.
- [**ConvertTo-PKISecureString**](.\docs\ConvertTo-PKISecureString.md) converts a previously encrypted SecureString back into a PowerShell SecureString object using the provided certificate's Private Key.
- [**Export-PSCredential**](.\docs\Export-PSCredential.md) encrypts and saves a PowerShell Credential object to file or to Azure KeyVault.
- [**Import-PSCredential**](.\docs\Import-PSCredential.md) decrypts a previously saved Credential back into a PowerShell Credential object.
- [**New-PSCredential**](.\docs\New-PSCredential.md) creates new PowerShell credential object, with a random strong password, and saves it to an encrypted file or to Azure KeyVault.
