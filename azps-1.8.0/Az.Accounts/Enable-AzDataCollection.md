---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751283"
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzDataCollection](./Disable-AzDataCollection.md)

