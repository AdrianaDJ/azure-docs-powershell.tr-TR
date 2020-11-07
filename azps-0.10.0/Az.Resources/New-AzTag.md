---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 242f207faa98c6165e4c64f095f9b171f1d72d5c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936381"
---
# New-AzTag

## SYNOPSIS
Önceden tanımlanmış bir Azure etiketi oluşturur veya varolan bir etikete değerler ekler.

## INDEKI

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzTag** cmdlet 'i önceden tanımlanmış bir önceden tanımlanmış değer Içeren bir Azure etiketi oluşturur.
Önceden tanımlanmış varolan etiketlere başka değerler eklemek için de kullanabilirsiniz.
Önceden tanımlanmış bir etiket oluşturmak için benzersiz bir etiket adı girin.
Önceden tanımlanmış varolan bir etikete değer eklemek için, varolan etiketin adını ve yeni değeri belirtin.
Bu cmdlet, değerleri ve uygulandığı kaynak sayısını temsil eden bir nesne döndürür.
**Yeni-AzTag** 'in bir parçası olduğu Azure Etiket modülü önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.
Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.
Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.
Kaynak veya kaynak grubuna önceden tanımlanmış bir etiket uygulamak için, New-AzTag cmdlet 'inin *etiket* parametresini kullanın.
Belirtilen etiket adı veya adı olan kaynak gruplarını aramak için, Get-AzResourceGroup cmdlet 'inin *etiket* parametresini kullanın.
Her etiketin bir adı vardır.
Değerler isteğe bağlıdır.
Önceden tanımlanmış bir Azure etiketinin birden çok değeri olabilir, ancak etiketi kaynak veya kaynak grubuna uyguladığınızda etiket adını ve yalnızca değerlerinden birini uygulayın.
Örneğin, finans, Insan kaynakları ve BT gibi her departman için bir değer içeren önceden tanımlanmış bir bölüm etiketi oluşturabilirsiniz.
Bir kaynağa departman etiketini uyguladığınızda, finans gibi yalnızca önceden tanımlanmış bir değer uygulaındı.

## ÖRNEKLERDEN

### Örnek 1: önceden tanımlanmış bir etiket oluşturma
```
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Bu komut, FY2015 adında önceden tanımlanmış bir etiket oluşturur.
Bu etikette değer yok.
Bir kaynak veya kaynak grubuna değer içermeyen bir etiket uygulayabilir veya etikete değer eklemek için **New-AzTag** 'i kullanabilirsiniz.
Etiketi kaynağa veya kaynak grubuna uyguladığınızda de bir değer belirtebilirsiniz.

### Örnek 2: bir değer içeren önceden tanımlanmış bir etiket oluşturma
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Bu komut, finans değeriyle bölüm adlı önceden tanımlanmış bir etiket oluşturur.

### Örnek 3: önceden tanımlanmış bir etikete değer ekleme
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Bu komutlar, iki değerli bölüm adlı önceden tanımlanmış bir etiket oluşturur.
Etiket adı varsa, **New-AzTag** , yeni bir tane oluşturmak yerine değeri varolan etikete ekler.

### Örnek 4: önceden tanımlanmış etiket kullanma
```
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

Bu örnekteki komutlar önceden tanımlanmış bir etiket oluşturur ve kullanılır.

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

### -Ad
Etiket adını belirtir.
Önceden tanımlanmış yeni bir etiket oluşturmak için benzersiz bir ad girin.
Var olan etikete değer eklemek için var olan etiketin adını girin.
Önceden bir önceden tanımlanmış etiketin belirtilen adı varsa, **New-AzTag** , varsa, yeni etiket oluşturmak yerine bu adı içeren etikete (varsa) ekler.

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

### -Değer
Etiket değeri belirtir.
Önceden tanımlanmış Etiketler birden çok değere sahip olabilir, ancak her komuta yalnızca bir değer girebilirsiniz.
Bu parametre isteğe bağlıdır; çünkü Etiketler değer içermeyen adlara sahip olabilir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

