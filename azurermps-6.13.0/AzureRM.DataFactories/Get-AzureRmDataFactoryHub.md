---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: d1015a5f401b0cb91731bafe93ead02e2bf3068f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594423"
---
# Get-AzureRmDataFactoryHub

## SYNOPSIS
Azure Veri Fabrikası 'nde Hub 'lar hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmDataFactoryHub** cmdlet 'ı Azure Veri Fabrikası 'ndaki Hublar hakkında bilgi alır.
Bir hub adı belirtirseniz, bu cmdlet bu hub hakkında bilgi alır.
Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm Hub 'lar hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: tüm veri hub 'ları
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

Bu komut, ADFResourceGroup adlı Azure Resource grubundaki tüm veri hub 'ları ve ADFDataFactory adlı veri fabrikası alır.

### Örnek 2: belirli bir veri hub 'ı edinin
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

Bu komut, ADFResourceGroup adlı Azure Resource grubunda MyDataHub adlı hub ve ADFDataFactory adlı veri fabrikası hakkında bilgi alır.

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki Hublar hakkında bilgi alır.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Veri Fabrikası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki Hublar hakkında bilgi alır.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Ad
Bilgi alınacak hub 'ın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait olan Hublar hakkında bilgi alır.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataFactory. modeller. PSHub

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmDataFactoryHub](./New-AzureRmDataFactoryHub.md)

[Remove-AzureRmDataFactoryHub](./Remove-AzureRmDataFactoryHub.md)


