---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 9536e6250f73270c7700a14406cb24b8e8f31189
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587097"
---
# Set-AzureRmTrafficManagerProfile

## SYNOPSIS
Traffic Manager profilini güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini güncelleştirir.
Bu cmdlet profili yerel bir profil nesnesinden güncelleştirir.
*TrafficManagerProfile* parametresini kullanarak veya ardışık düzeni kullanarak profil nesnesini belirtebilirsiniz.

Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak bir profili temsil eden yerel bir nesne edinebilirsiniz.
Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzureRmTrafficManagerProfile** kullanın.

## ÖRNEKLERDEN

### Örnek 1: profili güncelleştirme
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

İlk komut, Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.
Komut, profili yerel olarak $TrafficManagerProfile değişkeninde depolar.

İkinci komut bu profili yerel olarak değiştirir.
Bu komut profili devre dışı bırakır.

Üçüncü komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.

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

### -TrafficManagerProfile
Yerel bir **TrafficManagerProfile** nesnesi belirtir.
Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.

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
Bu cmdlet bir **TrafficManagerProfile** nesnesini kabul eder.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Bu cmdlet bir **TrafficManagerProfile** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)


