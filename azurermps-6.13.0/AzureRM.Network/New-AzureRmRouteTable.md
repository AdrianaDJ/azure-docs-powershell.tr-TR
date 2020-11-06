---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: fff89f2b6d37dc75923527fdb07a71d79dee80a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594366"
---
# New-AzureRmRouteTable

## SYNOPSIS
Yol tablosu oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation]
 -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmRouteTable** cmdlet 'ı bir Azure yol tablosu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: yol içeren bir yol tablosu oluşturma
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

İlk komut, New-AzureRmRouteConfig cmdlet 'ini kullanarak Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar. Bu yol paketleri yerel sanal ağa iletir.
İkinci komut RouteTable01 adlı bir yol tablosu oluşturur ve $Route depolanan yolu yeni tabloya ekler. Komut, tablonun ait olduğu kaynak grubunu ve tablonun konumunu belirtir.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

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

### -Disablebgprouteyayma
BGP Route otomatik yaymayı devre dışı bırakın.

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

### -Force
Aynı ada sahip bir yol tablosu var olsa bile bu cmdlet 'in bir yol tablosu oluşturduğunu gösterir.

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

### -Konum
Bu cmdlet 'in yol tablosu oluşturduğu Azure bölgesini belirtir.
Daha fazla bilgi için bkz [.](https://azure.microsoft.com/en-us/regions/)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Yol tablosu için bir ad belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in yol tablosu oluştururken kaynak grubun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Route
Yol tablosuyla ilişkilendirilecek bir **yol** nesneleri dizisi belirtir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

### System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. PSRoute, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSRouteTable

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[Yeni-AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[Remove-AzureRmRouteTable](./Remove-AzureRmRouteTable.md)

[Set-AzureRmRouteTable](./Set-AzureRmRouteTable.md)
