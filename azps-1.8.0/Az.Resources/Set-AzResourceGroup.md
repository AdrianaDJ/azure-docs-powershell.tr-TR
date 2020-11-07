---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 6e8a6cfe4e103588ac3f09d303bf517344573955
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759306"
---
# Set-AzResourceGroup

## SYNOPSIS
Kaynak grubunda değişiklik yapar.

## INDEKI

### SetByResourceGroupName (varsayılan)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Setbyresourcegroupıd
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzResourceGroup** cmdlet 'i, kaynak grubunun özelliklerini değiştirir.
Bu cmdlet 'i kaynak grubuna uygulanmış Azure etiketlerini eklemek, değiştirmek veya silmek için kullanabilirsiniz.
Etiketleri değiştirmek için kaynak grubunu ve *etiket* parametresini tanımlayacak *ad* parametresini belirtin.
Bu cmdlet 'i kaynak grubunun adını değiştirmek için kullanamazsınız.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubuna etiket uygulama
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Bu komut, mevcut etiketleri olmayan bir kaynak grubuna bir değer içeren bir departman etiketi uygular.

### Örnek 2: kaynak grubuna etiket ekleme
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Bu örnek, mevcut etiketleri olan kaynak grubuna onaylanmış bir değer ve bir FY2016 etiketi içeren bir durum etiketi ekler. Belirttiğiniz Etiketler var olan etiketlerin yerine, varolan etiketleri yeni etiket koleksiyonuna eklemeniz gerekir.
İlk komut ContosoRG kaynak grubunu alır ve etiket yöntemini kullanarak etiketleri özelliğinin değerini alır. Komut, etiketleri $Tags değişkeninde depolar.
İkinci komut $Tags değişkeninde etiketleri alır.
Üçüncü komut, FY2016 ve etiketlerini $Tags değişkeninde etiket dizisine eklemek için + = atama işlecini kullanır.
Dördüncü komut, $Tags değişkenindeki etiketleri ContosoRG kaynak grubuna uygulamak için **set-AzResourceGroup** *etiket* parametresini kullanır.
Beşinci komut, ContosoRG kaynak grubuna uygulanan tüm etiketleri alır. Çıktıda, kaynak grubunda bölüm etiketi ve iki yeni etiket, durum ve FY2015 bulunur.

### Örnek 3: kaynak grubun tüm etiketlerini silme
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Position: Named
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
Position: Named
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
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} etiket, kaynak ve kaynak gruplarına oluşturabileceğiniz ve uygulayabileceğiniz ad-değer çiftidir. Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzResource ve Get-AzResourceGroup *Etiket parametresini kullanarak* etiket adına veya adlarına göre kaynak ve grupları arayabilirsiniz. Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.
Etiket eklemek veya değiştirmek için, kaynak grubun etiket koleksiyonunu değiştirmelisiniz. Etiketi silmek için, silmek istediğiniz etiket **dışında, kaynak** grubuna şu anda kaynak grubuna uygulanmış olan tüm etiketlerin bulunduğu bir karma tablo girin. Kaynak grubundaki tüm etiketleri silmek için boş bir karma tablo belirtin: `@{}` .

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

### System. String

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[Yeni-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
