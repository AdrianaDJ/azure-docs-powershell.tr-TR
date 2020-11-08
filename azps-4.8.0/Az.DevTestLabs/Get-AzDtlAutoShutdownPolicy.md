---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 1b73ba8a313765488ba12b465a56542ca4b8b34a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273627"
---
# Get-AzDtlAutoShutdownPolicy

## SYNOPSIS
DevTest laboratuvarlarında bir laboratuvarın otomatik kapatma ilkesini alır.

## INDEKI

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzDtlAutoShutdownPolicy** cmdlet 'i, bir laboratuvarın otomatik kapatma ilkesini alır ve bu, belirli bir zamanda laboratuarda tüm sanal makineleri otomatik olarak kapatmanızı sağlar.
Cmdlet, ilkenin durumunun etkinleştirilip etkinleştirilmediğini ve günün saatini laboratuvar sanal makinelerini otomatik olarak kapatmak için ayarladığınız saat olarak döndürür.

## ÖRNEKLERDEN

### Örnek 1

DevTest laboratuvarlarında bir laboratuvarın otomatik kapatma ilkesini alır. oluşturulmuş

```powershell <!-- Aladdin Generated Example --> 
Get-AzDtlAutoShutdownPolicy -LabName <String> -ResourceGroupName MyResourceGroup
```

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -LabName
Bu cmdlet 'in otomatik kapatma ilkesini aldığı laboratuarın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Laboratuarın ait olduğu kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzDtlAutoShutdownPolicy](./Set-AzDtlAutoShutdownPolicy.md)


