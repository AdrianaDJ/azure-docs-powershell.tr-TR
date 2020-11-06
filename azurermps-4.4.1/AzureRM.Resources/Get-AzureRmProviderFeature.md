---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592587"
---
# Get-AzureRmProviderFeature

## SYNOPSIS
Azure sağlayıcı özellikleri hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ListAvailableParameterSet (varsayılan)
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetFeature
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmProviderFeature** cmdlet 'i Azure sağlayıcı özelliklerinin özellik adını, sağlayıcı adını ve kayıt durumunu alır.

## ÖRNEKLERDEN

### Örnek 1: kullanılabilir tüm özellikleri alma
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

Bu komut kullanılabilir tüm özellikleri alır.

### Örnek 2: belirli bir özellikle ilgili bilgileri alma
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

Bu komut, belirtilen sağlayıcı için AllowPreReleaseRegions adlı özelliğin bilgilerini alır.

## PARAMETRELERINE

### -FeatureName
Alınacak özelliğin adını belirtir.

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListAvailable
Bu cmdlet 'in tüm özellikleri aldığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProviderNamespace
Bu cmdlet 'in sağlayıcı özelliklerini aldığı ad boşluğunu belirtir.

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Register-AzureRmProviderFeature](./Register-AzureRmProviderFeature.md)


