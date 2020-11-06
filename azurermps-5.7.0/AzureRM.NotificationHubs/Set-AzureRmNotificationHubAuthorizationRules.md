---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 6203c5554dcdbfbd40c861a3f73e1a5947228030
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594913"
---
# Set-AzureRmNotificationHubAuthorizationRules

## SYNOPSIS
Bildirim Hub 'ına yönelik yetkilendirme kurallarını ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Inputfileparameterset
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub 'ına atanan paylaşılan erişim IMZASıNı (SAS) yetkilendirme kuralını değiştirir.

Yetkilendirme kuralları, farklı izin düzeylerine dayalı olarak, bağlantı oluşturarak Bildirim Hub 'larına erişimi yönetir.
İzin düzeyleri aşağıdakilerden biri olabilir: 

- Sten
- Gönder
- Yönetebilirsiniz

İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.
Örneğin, dinleme izni verilen bir istemci bu izin için URI 'ye yönlendirilir.

Bu cmdlet, Bildirim Hub 'ına atanmış yetkilendirme kuralını değiştirmek için iki yol sağlar.
Bir tane için, **Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.
Nesneyi .NET Framework aracılığıyla yapılandırabilirsiniz.
Bu özellik değerlerini, *sasrule* parametresini kullanarak kuralınıza kopyalayabilirsiniz.

Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.
JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır:

{"Ad": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "Haklar": \[  
        "Dinle",  
        Göndermek  
    \]  
}

New-AzureRmNotificationHubAuthorizationRules cmdlet 'le birlikte kullanıldığında, önceki JSON örneği, kullanıcılara, hub 'a Kullanıcı dinlemesi ve gönderimi izni vermek için ContosoAuthorizationRule adlı bir yetkilendirme kuralını değiştirir.

## ÖRNEKLERDEN

### Örnek 1: Bildirim Hub 'ına atanan yetkilendirme kuralını değiştirme
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Bu komut, ContosoExternalHub adlı Bildirim Hub 'ına atanmış yetkilendirme kuralını değiştirir.
Hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.
Değiştirilen kuralla ilgili bilgiler komuta dahil değildir.
Bunun yerine bu bilgiler C:\Configuration\AuthorizationRules.jsgiriş dosyasında bulunur.

## PARAMETRELERINE

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

### -Force
Onay sorma.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GirdiDosyası
Yeni kuralın yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.
Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
Bu cmdlet 'in yetkilendirme kuralları atadığı Bildirim Merkezi 'ni belirtir.
Bildirim hubları, bu istemciler tarafından kullanılan bağımsız olarak birden fazla istemciye anında bildirim göndermek için kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Bildirim Hub 'ına atanmış kaynak grubunu belirtir. Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SASRule
Değiştirilen yetkilendirme kuralları için yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Yeni-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)


