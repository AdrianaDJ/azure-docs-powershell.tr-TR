---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268586"
---
# New-AzVmssVaultCertificateConfig

## SYNOPSIS
Anahtar Kasası sertifikası yapılandırması oluşturur.

## INDEKI

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzVmssVaultCertificateConfig** cmdlet 'Inin sanal makine ölçek KÜMESI (VMSS) sanal makinelerine yerleştirilmesi gereken parolayı belirtir.
Bu cmdlet 'in çıktısı Add-AzVmssSecret cmdlet ile kullanılmak üzere tasarlanmıştır.

## ÖRNEKLERDEN

### Örnek 1: Anahtar Kasası sertifikası yapılandırması oluşturma
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

Bu komut, belirtilen sertifika URL 'sinde bulunan mycert adındaki sertifika deposunu kullanan bir Anahtar Kasası sertifikası yapılandırması oluşturur.

## PARAMETRELERINE

### -CertificateStore
Sanal makinelerde, sertifikanın eklendiği ölçek kümesindeki sertifika deposunu belirtir.
Bu yalnızca Windows sanal makine ölçek kümeleri için geçerlidir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl 'Si
Anahtar kasasına depolanan bir sertifikanın URI 'sini belirtir.
UTF-8 ile kodlanmış olan aşağıdaki JSON nesnesinin Base64 kodlamasıdır: {"Data": " \<Base64-encoded-certificate\> ", "DataType": "PFX", "Password": " \<pfx-file-password\> "}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Management. COMPUTE. modeller. VaultCertificate

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzVmssSecret](./Add-AzVmssSecret.md)
