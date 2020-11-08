---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108765"
---
# Get-AzTag

## SYNOPSIS
Önceden tanımlanmış Azure etiketlerini alır | Kaynağın veya aboneliğin tüm etiket kümesini alır.

## INDEKI

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyresourceıdparameterset
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım

**Getpredefinedtagset** : **Get-aztag** cmdlet 'i aboneliğinizdeki önceden tanımlanmış Azure etiketlerini alır.
Bu cmdlet etiketlerle ilgili temel bilgileri veya Etiketler ile değerleriyle ilgili ayrıntılı bilgileri döndürür.
Tüm çıktı nesneleri, etiketlerin ve değerlerin uygulandığı kaynak ve kaynak gruplarının sayısını temsil eden bir say özelliği içerir.
**Get-AzTag** 'in bir parçası olduğu Azure Etiket modülü önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.
Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.
Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.
Önceden tanımlanmış bir etiket oluşturmak için New-AzTag cmdlet 'ini kullanın.
Kaynak grubuna önceden tanımlanmış bir etiket uygulamak için New-AzTag cmdlet 'inin *etiket* parametresini kullanın.
Belirli bir etiket adı veya adı ve değerinin kaynak gruplarını aramak için, Get-AzResourceGroup cmdlet 'inin *etiket* parametresini kullanın.

**Getbyresourceıdparameterset** : **RESOURCEID** Içeren **Get-aztag** cmdlet 'i, bir kaynak veya abonelikteki tüm etiket kümesini alır.

## ÖRNEKLERDEN

### Örnek 1: tüm önceden tanımlanmış etiketleri alma
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Bu komut, abonelikteki tüm önceden tanımlanmış etiketleri alır.
Count özelliği, etiketlerin, abonelikteki kaynaklara ve kaynak gruplarına kaç kez uygulandığını gösterir.

### Örnek 2: ada göre etiket alma
```powershell
PS C:\>Get-AzTag -Name "Department"

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
```powershell
PS C:\>Get-AzTag -Detailed

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

### Örnek 4: bir abonelikteki tüm etiket kümesini alma

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Bu komut, {subId} ile abonelikteki tüm etiket kümesini alır.

### Örnek 5: kaynaktaki tüm etiket kümesini alma

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Bu komut, {RESOURCEID} ile kaynaktaki tüm etiket kümesini alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Önceden tanımlanmış etiketin adı.
**Get-AzTag** , varsayılan olarak, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili temel bilgileri alır.
*Name* parametresini belirttiğinizde, *ayrıntılı* parametrenin etkisi yoktur.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Etiketli varlık için kaynak tanımlayıcısı. Kaynak, kaynak grubu veya abonelik etiketleniyor olabilir.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
