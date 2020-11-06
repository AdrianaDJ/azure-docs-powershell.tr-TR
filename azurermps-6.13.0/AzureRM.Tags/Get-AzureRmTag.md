---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594323"
---
# Get-AzureRmTag

## SYNOPSIS
Önceden tanımlanmış Azure etiketlerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmTag** cmdlet 'i aboneliğinizdeki önceden tanımlanmış Azure etiketlerini alır.
Bu cmdlet etiketlerle ilgili temel bilgileri veya Etiketler ile değerleriyle ilgili ayrıntılı bilgileri döndürür.
Tüm çıktı nesneleri, etiketlerin ve değerlerin uygulandığı kaynak ve kaynak gruplarının sayısını temsil eden bir say özelliği içerir.
**Get-AzureRMTag** 'in bir parçası olduğu Azure Etiket modülü, önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.
Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.
Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.
Önceden tanımlanmış bir etiket oluşturmak için New-AzureRmTag cmdlet 'ini kullanın.
Kaynak grubuna önceden tanımlanmış bir etiket uygulamak için New-AzureRmTag cmdlet 'inin *etiket* parametresini kullanın.
Belirli bir etiket adı veya adı ve değerinin kaynak gruplarını aramak için, Get-AzureRMResourceGroup cmdlet 'inin *etiket* parametresini kullanın.

## ÖRNEKLERDEN

### Örnek 1: tüm önceden tanımlanmış etiketleri alma
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Bu komut, abonelikteki tüm önceden tanımlanmış etiketleri alır.
Count özelliği, etiketlerin, abonelikteki kaynaklara ve kaynak gruplarına kaç kez uygulandığını gösterir.

### Örnek 2: ada göre etiket alma
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Bu komut, Bölüm etiketi ve değerleri hakkında ayrıntılı bilgi alır.
Count özelliği, etiketlerin ve bu değerlerin her birinin abonelikteki kaynaklara ve kaynak gruplarına uygulanma sayısını gösterir.

### Örnek 3: tüm etiketlerin değerlerini alma
```
PS C:\>Get-AzureRmTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Bu komut, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili ayrıntılı bilgi almak için *ayrıntılı* parametreyi kullanır.
*Detailed* parametresini kullanmak, her etiket için *Name* parametresini kullanmanın eşdeğeridir.

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

### -Ayrıntılı
Bu işlemin çıktıya etiket değerleri hakkında bilgi eklediği anlamına gelir.

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

### -Ad
Alınacak etiketin adını belirtir.
**Get-AzureRmTag** varsayılan olarak, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili temel bilgileri alır.
*Name* parametresini belirttiğinizde, *ayrıntılı* parametrenin etkisi yoktur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmTag](./New-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


