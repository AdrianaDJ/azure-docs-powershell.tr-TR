---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 1481b577e248354eb2fdccbb9d6ecd450ab0cf62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595138"
---
# Disable-AzureRmTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager profilindeki uç noktayı devre dışı bırakır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Alanlardır
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Nesnelerini
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Disable-AzureRmTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profilindeki uç noktayı devre dışı bırakır.

**TrafficManagerEndpoint** nesnesini bu cmdlet 'e geçirmek için ardışık düzen işlecini kullanabilir ya da *TrafficManagerEndpoint* parametresini kullanarak **TrafficManagerEndpoint** nesnesini geçirebilirsiniz.

Alternatif olarak, *ProfilAdı* ve *Resourcegroupname* parametreleriyle *ad* ve *tür* parametrelerini kullanarak uç nokta adını ve türünü de belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: uç noktayı adıyla devre dışı bırakma
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Bu komut, kaynak grubu ResouceGroup11 ContosoProfile adlı profildeki contoso adlı dış uç noktasını devre dışı bırakır.
Komut sizden onaylamanızı ister.

### Örnek 2: ardışık düzeni kullanarak uç noktayı devre dışı bırakma
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

Bu komut, ResourceGroup11 'daki ContosoProfile adlı profilden contoso adlı dış uç noktayı alır.
Komut daha sonra bu uç noktayı, ardışık düzen işlecini kullanarak **Disable-AzureRmTrafficManagerEndpoint** cmdlet 'ine geçirir.
Bu cmdlet uç noktayı devre dışı bırakır.
Komut *Force* parametresini belirtir.
Bu nedenle sizden onay istemez.

## PARAMETRELERINE

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in devre dışı olduğu Traffic Manager uç noktasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Bu cmdlet 'in uç noktayı devre dışı bırakabildiği bir Traffic Manager profilinin adını belirtir.
Profil edinmek için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager uç noktasını devre dışı bırakır.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Bu cmdlet 'in devre dışı olduğu Traffic Manager uç noktasını belirtir.
**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tür
Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.
Geçerli değerler: 

- AzureEndpoints
- ExternalEndpoints
- Nestedenvseçpuanlar

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### TrafficManagerEndpoint
' TrafficManagerEndpoint ' parametresi ardışık düzen için ' TrafficManagerEndpoint ' türünün değerini kabul eder

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Enable-AzureRmTrafficManagerEndpoint](./Enable-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerEndpoint](./Get-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


