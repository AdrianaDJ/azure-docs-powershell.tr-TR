---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 1c7f55bb3f84051326cd102c1c12a2d978a79f71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764584"
---
# Remove-AzureRmTag

## SYNOPSIS
Önceden tanımlanmış Azure etiketlerini veya değerlerini siler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmTag** cmdlet 'i aboneliğinizden önceden tanımlanmış Azure etiketlerini ve değerlerini siler.
Önceden tanımlanmış bir etiketten belirli değerleri silmek için, *değer* parametresini kullanın.
Varsayılan olarak, **Remove-AzureRmTag** belirtilen etiketi ve tüm değerlerini siler. Bir kaynağa veya kaynak grubuna uygulanmış olan bir etiketi veya değeri silemezsiniz.
**Remove-AzureRmTag** 'i kullanmadan önce, kaynak veya kaynak grubundan etiket veya değerleri silmek için Set-AzureRMResourceGroup cmdlet 'in *etiket* parametresini kullanın.
**-AzureRmTag** 'in parçası olan Azure Etiket modülü, önceden tanımlanmış Azure etiketlerinizi yönetmenize yardımcı olabilir.
Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.
Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.

## ÖRNEKLERDEN

### Örnek 1: önceden tanımlanmış bir etiketi silme
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

Bu komut, Bölüm adlı önceden tanımlanmış etiketi ve tüm kaynaklarını siler.
Etiket herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.

### Örnek 2: önceden tanımlanmış etiketten bir değer silme
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Bu komut, önceden tanımlanmış Departman etiketinden HumanResources değerini siler.
Etiketi silmez.
Değer herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.

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

### -Ad
Silinecek etiketin adını belirtir.
Varsayılan olarak, **Remove-AzureRmTag** belirtilen etiketi ve tüm değerlerini kaldırır.
Seçili değerleri silmek, ancak etiketi silistemiyorsanız *değer* parametresini kullanın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Silinmiş etiketi veya sonuç etiketine sahip olan sonuç etiketini temsil eden bir nesne döndürür.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Değer
Önceden tanımlanmış etiketten belirtilen değerleri siler, ancak etiketi silmez.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### System. String []

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Yeni-AzureRmTag](./New-AzureRmTag.md)


