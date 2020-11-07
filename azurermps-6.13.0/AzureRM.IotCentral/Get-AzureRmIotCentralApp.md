---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764955"
---
# Get-AzureRmIotCentralApp

## SYNOPSIS
Bir veya birkaç IoT Merkezi uygulamasının özelliklerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ListIotCentralAppsParameterSet (varsayılan)
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Interactiveıotmerkezileştirme Parametrekümesi
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceıdparameterset
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Belirli bir IoT Merkezi uygulamasının meta verilerini veya parametre kümesine bağlı olarak bir kaynak grubundaki veya abonelikteki tüm uygulamaları alır. 

## ÖRNEKLERDEN

### Örnek 1 belirli IoT Merkezi uygulaması alın.
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Belirtilen IoT Merkezi uygulamasının meta verilerini alır.

Örnek çıktı:

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName

### Örnek 2;
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

Geçerli abonelikteki tüm IoT merkezi uygulamaları için meta verileri alır.

Örnek çıktı:

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName2 adı: MyAppResourceName2 türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId 1 alt etki alanı: MyAppSubdomain2 Template: SubscriptionID: XXXXXXXX-xxxx-xxxx-xxxx- iotc-default@1.0.0 xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2

### Örnek 3 kaynak grubunda IoT merkezi uygulamalarını alın.
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Sağlanan kaynak grubundaki tüm IoT merkezi uygulamaları için meta verileri alır.

Örnek çıktı:

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName

RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName2 adı: MyAppResourceName2 türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (XXXXXXXX): MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

## PARAMETRELERINE

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
IoT Merkezi uygulama kaynağının adı.

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
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
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
IoT Merkezi uygulama kaynak kimliği.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String
## ÇıKıŞLAR

### Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp
## NOTLARıNDA

## ILGILI BAĞLANTıLAR
