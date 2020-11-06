---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571030"
---
# Import-AzureRmContext

## SYNOPSIS
Azure kimlik doğrulama bilgilerini dosyadan yükler.

## INDEKI

### Inmemoryprofile
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### ProfileFromDisk
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## Tanım
Import-AzureRmContext cmdlet, Azure ortamı ve bağlamını ayarlamak için bir dosyadan kimlik doğrulama bilgilerini yükler.
Geçerli oturumda çalıştırdığınız cmdlet 'ler, Azure Resource Manager 'daki isteklerin kimlik doğrulaması için bu bilgileri kullanır.

## ÖRNEKLERDEN

### Örnek 1: AzureRmProfile bir bağlam Içeri aktarma
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Bu örnek, cmdlet 'e geçirilen PSAzureProfile 'daki bir bağlamı içeri aktarır.

### Örnek 2: JSON dosyasındaki bağlamı Içeri aktarma
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Bu örnek, cmdlet 'e geçirilen JSON dosyasından bir bağlam seçer.
Bu JSON dosyası Import-AzureRmContext 'ten oluşturulabilir.

## PARAMETRELERINE

### -AzureContext
Bu cmdlet 'in okuduğu Azure bağlamını belirtir.
Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Save-AzureRMContext kullanılarak kaydedilen bağlam bilgilerinin yolunu belirtir.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
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

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRMProfile
System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

