---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764615"
---
# New-AzureRmFirewallApplicationRuleCollection

## SYNOPSIS
Güvenlik Duvarı uygulama kuralları koleksiyonu oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmFirewallApplicationRuleCollection** cmdlet 'ı, güvenlik duvarı uygulama kuralları koleksiyonu oluşturur.

## ÖRNEKLERDEN

### 1: tek kuralla koleksiyon oluşturma
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

Bu örnek bir kural içeren bir koleksiyon oluşturur. $Rule 1 ' de belirtilen koşullara uyan tüm trafiğe izin verilir.
İlk kural, 10.0.0.0 ile bağlantı noktası 443 üzerindeki tüm HTTPS trafiği içindir. Daha yüksek önceliğe sahip başka bir uygulama kuralı koleksiyonu varsa $rule 1 ' de tanımlanan trafikle de eşleşir; bunun yerine, kural koleksiyonunun yüksek önceliğe sahip eylemi geçerli olacaktır. 

### 2: kural koleksiyonuna kural ekleme
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

Bu örnek, bir kuralla yeni bir uygulama kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural ekler. Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.

### 3: kural koleksiyonundan kural alma
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

Bu örnek, bir kuralla yeni bir uygulama kuralı koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır. GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.

### 4: kural koleksiyonundan kural kaldırma
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

Bu örnekte, iki kural içeren yeni bir uygulama kuralı koleksiyonu oluşturulur ve kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan ilk kuralı kaldırır. Yöntem için kural adı, büyük/küçük harf duyarlı değildir.

## PARAMETRELERINE

### -ActionType
Kural koleksiyonunun eylemi

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Ad
Bu uygulama kuralının adını belirtir. Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Öncelik
Bu kuralın önceliğini belirtir. Öncelik, 100 ve 65000 arasındaki bir sayıdır. Sayı ne kadar küçükse öncelik o kadar büyük olur.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kural
Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
Parameter Sets: (All)
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSFirewallApplicationRuleCollection

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmFirewallApplicationRule](./New-AzureRmFirewallApplicationRule.md)

[Yeni-AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)
