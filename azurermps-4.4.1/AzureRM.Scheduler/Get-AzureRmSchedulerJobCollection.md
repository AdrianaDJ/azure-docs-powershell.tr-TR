---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594568"
---
# Get-AzureRmSchedulerJobCollection

## SYNOPSIS
İş koleksiyonlarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmSchedulerJobCollection** cmdlet 'ı Azure Scheduler 'daki iş koleksiyonlarını alır.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -JobCollectionName
İş koleksiyonunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in iş koleksiyonlarını aldığı kaynak grubunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### System. Object

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzureRmSchedulerJobCollection](./Disable-AzureRmSchedulerJobCollection.md)

[Enable-AzureRmSchedulerJobCollection](./Enable-AzureRmSchedulerJobCollection.md)

[New-AzureRmSchedulerJobCollection](./New-AzureRmSchedulerJobCollection.md)

[Remove-AzureRmSchedulerJobCollection](./Remove-AzureRmSchedulerJobCollection.md)

[Set-AzureRmSchedulerJobCollection](./Set-AzureRmSchedulerJobCollection.md)


