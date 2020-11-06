---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: d93dadc062f2cc12ed363039d69266daf365920e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587655"
---
# Get-AzureRmCdnProfileSsoUrl

## SYNOPSIS
CDN profilinin çoklu oturum açma URL 'sini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFieldsParameterSet (varsayılan)
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectParameterSet
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmCdnProfileSsoUrl** cmdlet 'ı, Azure Içerik teslim ağı (CDN) profilinin çoklu oturum açma URL 'sini alır.
Bu URL, kullanıcıların bir destek portalına ulaşmanızı ve CDN 'nin ek özelliklerini kullanmasını sağlar.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -CdnProfile
CDN profilini belirtir.

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

### -ProfileName
CDN profilinin adını belirtir.

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
Profilin ait olduğu kaynak grubu adının adını belirtir.

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
Bu cmdlet bir URL döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRMCdnProfile](./Get-AzureRMCdnProfile.md)


