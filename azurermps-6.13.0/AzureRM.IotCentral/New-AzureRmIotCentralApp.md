---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594890"
---
# New-AzureRmIotCentralApp

## SYNOPSIS
Yeni bir IoT Merkezi uygulaması oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Sağlanan özellikler ve meta veriler ile yeni bir IoT Merkezi uygulaması oluşturur. IoT merkezi 'ne giriş için bkz https://docs.microsoft.com/en-us/azure/iot-central/ .

## ÖRNEKLERDEN

### Örnek 1 basit IoT Merkezi uygulaması oluşturun.
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

Örnek çıktı:

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus etiket: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: MyApp-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 DisplayName:

Standart fiyatlandırma katmanı S1 içinde kaynak grubunun bölgesinde bir IoT Merkezi uygulaması oluşturun.

### Örnek 2 basit IoT Merkezi uygulaması oluşturun.
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

Örnek çıktı:

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus etiket: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: Dizinim-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 DisplayName:

' Westus ' bölgesinde, ıotc-default şablonunu temel alan özel bir görünen ad ile standart fiyatlandırma katmanı S1 ile IoT Merkezi uygulaması oluşturun.

## PARAMETRELERINE

### -Iş
Cmdlet 'i arka planda iş olarak çalıştırın.

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

### -DisplayName
IoT Merkezi uygulaması için özel görünen ad.
Varsayılan kaynak adıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
IoT merkezi uygulamanızın konumu.
Varsayılan hedef kaynak grubunun konumudur.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
IoT Merkezi uygulama kaynağının adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
IoT merkezi uygulamaları için fiyatlandırma katmanı.
Varsayılan değer S1 değeridir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Alt etki alanı
IoT merkezi URL 'SI için alt etki alanı.
Her uygulamanın benzersiz bir alt etki alanı olmalıdır.

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

### Etiketli
IoT Merkezi uygulama kaynağı etiketleri.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Şablon
IoT Merkezi uygulama şablonu adı.
Varsayılan özel bir uygulamadır.

```yaml
Type: String
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
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

### System. String
### System. topluluklar. Hashtable
## ÇıKıŞLAR

### Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp
## NOTLARıNDA

## ILGILI BAĞLANTıLAR
