---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764482"
---
# Get-AzureRmVMAEMExtension

## SYNOPSIS
AEM uzantısı hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısı hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: AEM uzantısını alma
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Bu komut contoso-Server adlı sanal makinenin AEM uzantısı için bilgileri alır.

## PARAMETRELERINE

### -Ad
Sanal makinenin adını belirtir.
Bu cmdlet, bu cmdlet 'in belirttiği sanal makinedeki AEM uzantısı için bilgileri alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
İşletim sistemi diskinin işletim sisteminin türünü belirtir.
İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.
Bu parametre için kabul edilebilir değerler: Windows ve Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.
Bu cmdlet, bu sanal makinedeki AEM uzantısı için bilgi alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Durum
Bu cmdlet 'in yalnızca AEM uzantısının örnek görünümünü aldığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Sanal makinenin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısı hakkında bilgi alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)

[Test-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


