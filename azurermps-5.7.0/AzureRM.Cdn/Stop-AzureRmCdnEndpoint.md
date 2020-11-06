---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587640"
---
# Stop-AzureRmCdnEndpoint

## SYNOPSIS
CDN uç noktasını durdurur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFieldsParameterSet (varsayılan)
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Stop-AzureRmCdnEndpoint** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktasını durdurur.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -CdnEndpoint
Bu cmdlet 'in durduğu uç nokta nesnesini belirtir.

```yaml
Type: PSEndpoint
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
Bu cmdlet 'in durdurduğu uç noktasının adını belirtir.

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

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
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

### PSEndpoint
Parametre ' CdnEndpoint ', ardışık düzen

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmCdnEndpoint](./Get-AzureRmCdnEndpoint.md)

[Yeni-AzureRmCdnEndpoint](./New-AzureRmCdnEndpoint.md)

[Remove-AzureRmCdnEndpoint](./Remove-AzureRmCdnEndpoint.md)

[Set-AzureRmCdnEndpoint](./Set-AzureRmCdnEndpoint.md)

[Start-AzureRmCdnEndpoint](./Start-AzureRmCdnEndpoint.md)


