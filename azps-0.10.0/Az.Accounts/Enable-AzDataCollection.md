---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: c9cfd91ecc094ad5df98d3c8478d197fbfa98a15
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935264"
---
# Enable-AzDataCollection

## SYNOPSIS
AzurePowerShell cmdlet 'leriyle Kullanıcı deneyimini geliştirmek için Azure PowerShell 'in veri toplamasını olanaklı kılar.
Geçerli bilgisayarda geçerli kullanıcının veri koleksiyonunda bu cmdlet 'i yürütme.
Açıkça kabul edilmedikçe veri toplanmaz.

## INDEKI

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.
Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi sorduğunda, açıkça kabul etmelisiniz.
Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.
Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.
Geçerli makinedeki geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzDataCollection cmdlet 'ini çalıştırın.
Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.
Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzDataCollection cmdlet 'ini çalıştırın.

## ÖRNEKLERDEN

### Örnek 1: geçerli kullanıcı için veri toplamayı etkinleştirme
```
PS C:\> Enable-AzDataCollection
```

Bu örnekte, geçerli kullanıcı için veri toplamayı etkinleştirme gösterilmektedir.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzDataCollection](./Disable-AzDataCollection.md)

