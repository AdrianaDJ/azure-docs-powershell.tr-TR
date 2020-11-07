---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 07e565031a5c29ae1be78246cad95326952007e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935237"
---
# Save-AzContext

## SYNOPSIS
Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.

## INDEKI

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Save-AzContext cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.

## ÖRNEKLERDEN

### Örnek 1: geçerli oturumun içeriği kaydediliyor
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

Bu örnek, geçerli oturumun Azure bağlamını sağlanan JSON dosyasına kaydeder.

### Örnek 2: verilen bağlamı kaydetme
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

Bu örnek, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure bağlamını kaydeder.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.

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

### -Force
Varsa, verilen dosyanın üzerine yaz

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure bağlamını belirtir.
Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

### Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRmProfile

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
