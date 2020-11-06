---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589700"
---
# Get-AzureRmReservationOrder

## SYNOPSIS
Al `ReservationOrder`

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## Tanım
`ReservationOrder`Kullanıcının geçerli kiracıda erişimi olan tüm s listesi. Rezervdeğer = parametre ayarlanmışsa, bu belirli Rezervtalebi siparişini alın.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmReservationOrder
```

`ReservationOrder`Kullanıcının geçerli kiracıya erişiminin olduğu tüm liste

### Örnek 2
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

`ReservationOrder`Belirtilen Rezervorderıd siparişiyle birlikte

## PARAMETRELERINE

### -Rezervationorderıd
Kullanıcının görmek istediği belirli Rezervsırası kodu

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage
Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

