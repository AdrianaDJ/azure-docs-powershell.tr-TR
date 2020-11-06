---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3468730caa727c7c8cde46ddbf431c374361b8fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587104"
---
# Remove-AzureRmTrafficManagerEndpointConfig

## SYNOPSIS
Yerel Traffic Manager profil nesnesinden uç noktayı kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmTrafficManagerEndpointConfig** cmdlet 'ı yerel Azure Traffic Manager profil nesnesinden bir uç noktayı kaldırır.
Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak profil alabilirsiniz.

Bu cmdlet yerel profil nesnesinde çalışır.
Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.
Uç noktayı kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: uç noktayı kaldırma
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.
Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.

İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden contoso adlı bir Azure uç noktasını kaldırır.
Bu komut yalnızca yerel nesneyi değiştirir.

Son komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.

## PARAMETRELERINE

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

### -EndpointName
Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Yerel bir **TrafficManagerProfile** nesnesi belirtir.
Bu cmdlet bu yerel nesneyi değiştirir.
**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Bu cmdlet değiştirilmiş bir TrafficManagerProfile nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


