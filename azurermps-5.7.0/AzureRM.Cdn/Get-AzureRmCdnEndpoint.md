---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587658"
---
# Get-AzureRmCdnEndpoint

## SYNOPSIS
CDN uç noktasını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFieldsParameterSet (varsayılan)
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectParameterSet
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRMCdnEndpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktasını ve ilişkili yapılandırma verilerini alır.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -CdnProfile
Uç noktanın ait olduğu CDN profili nesnesini belirtir.

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Uç noktasının adını belirtir.
Uç noktasının adı uç noktasının ana bilgisayar adı değildir.

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

### -ProfileName
Uç noktanın ait olduğu profilin adını belirtir.

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Uç noktanın ait olduğu kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### PSProfile
' CdnProfile ' parametresi ardışık düzenin ' PSProfile ' türünün değerini kabul eder

## ÇıKıŞLAR

###  
Bu cmdlet bir uç nokta nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmCdnEndpoint](./New-AzureRmCdnEndpoint.md)

[Remove-AzureRmCdnEndpoint](./Remove-AzureRmCdnEndpoint.md)

[Set-AzureRmCdnEndpoint](./Set-AzureRmCdnEndpoint.md)

[Start-AzureRmCdnEndpoint](./Start-AzureRmCdnEndpoint.md)

[Stop-AzureRmCdnEndpoint](./Stop-AzureRmCdnEndpoint.md)


