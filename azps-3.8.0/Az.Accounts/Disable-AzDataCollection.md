---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/30/2020
ms.locfileid: "94105080"
---
# Disable-AzDataCollection

## SYNOPSIS
Azure PowerShell cmdlet 'lerini geliştirmek için veri toplama dışında. Siz açıkça geri belirtmediğiniz sürece veriler varsayılan olarak toplanır.

## INDEKI

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım

`Disable-AzDataCollection`Cmdlet veri toplamayı geri çevirmek için kullanılır. Azure PowerShell varsayılan olarak telemetri verilerini otomatik olarak toplar. Veri toplamayı devre dışı bırakmak için, açıkça geri almalısınız. Microsoft, kullanım düzenlerini belirlemek, yaygın sorunları belirlemek ve Azure PowerShell 'in deneyimini geliştirmek için toplanan verileri toplar. Microsoft Azure PowerShell hiçbir özel veya kişisel veri toplamaz. Daha önce kabul ettiyseniz, `Enable-AzDataCollection` geçerli makinedeki geçerli kullanıcının veri toplamayı yeniden etkinleştirmek için cmdlet 'i çalıştırın.

## ÖRNEKLERDEN

### Örnek 1: geçerli kullanıcı için veri toplamayı devre dışı bırakma

Aşağıdaki örnekte, geçerli kullanıcı için veri toplamayı devre dışı bırakma gösterilmiştir.

```powershell
Disable-AzDataCollection
```

## PARAMETRELERINE

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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
