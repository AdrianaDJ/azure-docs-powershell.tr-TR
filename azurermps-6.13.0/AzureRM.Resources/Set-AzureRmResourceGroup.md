---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: 4ba57d1f8e1abe8c506f1bcd6625a7a90551f164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593896"
---
# Set-AzureRmResourceGroup

## SYNOPSIS
Kaynak grubunda değişiklik yapar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SetByResourceGroupName (varsayılan)
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Setbyresourcegroupıd
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzureRmResourceGroup** cmdlet 'i, kaynak grubunun özelliklerini değiştirir.
Bu cmdlet 'i kaynak grubuna uygulanmış Azure etiketlerini eklemek, değiştirmek veya silmek için kullanabilirsiniz.
Etiketleri değiştirmek için kaynak grubunu ve *etiket* parametresini tanımlayacak *ad* parametresini belirtin.
Bu cmdlet 'i kaynak grubunun adını değiştirmek için kullanamazsınız.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubuna etiket uygulama
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Bu komut, mevcut etiketleri olmayan bir kaynak grubuna bir değer içeren bir departman etiketi uygular.

### Örnek 2: kaynak grubuna etiket ekleme
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

Bu örnek, mevcut etiketleri olan kaynak grubuna onaylanmış bir değer ve bir FY2016 etiketi içeren bir durum etiketi ekler. Belirttiğiniz Etiketler var olan etiketlerin yerine, varolan etiketleri yeni etiket koleksiyonuna eklemeniz gerekir.
İlk komut ContosoRG kaynak grubunu alır ve etiket yöntemini kullanarak etiketleri özelliğinin değerini alır. Komut, etiketleri $Tags değişkeninde depolar.
İkinci komut $Tags değişkeninde etiketleri alır.
Üçüncü komut, FY2016 ve etiketlerini $Tags değişkeninde etiket dizisine eklemek için + = atama işlecini kullanır.
Dördüncü komut, ContosoRG kaynak grubuna $Tags değişkeninde etiketleri uygulamak için **set-AzureRmResourceGroup** *etiket* parametresini kullanır.
Beşinci komut, ContosoRG kaynak grubuna uygulanan tüm etiketleri alır. Çıktıda, kaynak grubunda bölüm etiketi ve iki yeni etiket, durum ve FY2015 bulunur.

### Örnek 3: kaynak grubun tüm etiketlerini silme
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

Bu komut, ContosoRG kaynak grubundaki tüm etiketleri silmek için boş karma tablo değeri olan *Tag* parametresini belirtir.

## PARAMETRELERINE

### -Apıversion
Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.
Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -ID
Değiştirilecek kaynak grubunun KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Değiştirilecek kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre-
Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.

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

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} etiket, kaynak ve kaynak gruplarına oluşturabileceğiniz ve uygulayabileceğiniz ad-değer çiftidir. Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzureRmResource ve Get-AzureRmResourceGroup *Etiket parametresini kullanarak* etiket adına veya adlarına göre kaynak ve grupları arayabilirsiniz. Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.
Etiket eklemek veya değiştirmek için, kaynak grubun etiket koleksiyonunu değiştirmelisiniz. Etiketi silmek için, silmek istediğiniz etiket dışında **Get-AzureRmResourceGroup** kaynağından, şu anda kaynak grubuna uygulanmış olan bir karma tablo girin. Kaynak grubundaki tüm etiketleri silmek için boş bir karma tablo belirtin: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. PSResourceGroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Yeni-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)
