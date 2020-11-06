---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: 0912ba8913bae430c3878dc0bde578420a5ea429
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587280"
---
# Get-AzureRmCdnOrigin

## SYNOPSIS
CDN kaynak sunucusunu alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFieldsParameterSet (varsayılan)
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectParameterSet
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermcvseçnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusu ve yapılandırma verilerini alır.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -CdnEndpoint
Başlangıcının ait olduğu CDN uç noktası nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Kaynak sunucunun ait olduğu uç noktasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdName
Kaynak sunucunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Kaynak sunucunun ait olduğu profilin adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.

```yaml
Type: System.String
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

### Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint
Parametreler: CdnEndpoint (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. CDN. model. Origin. Psorigın

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-Azurermcvseçnorigın](./Set-AzureRmCdnOrigin.md)


