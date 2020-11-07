---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: dd115a7d0445a7b07557b884dd2c7413f5269d00
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939850"
---
# New-AzureRmResourceGroup

## SYNOPSIS
Bir Azure Kaynak grubu oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmResourceGroup** cmdlet 'ı bir Azure Kaynak grubu oluşturur.
Yalnızca bir ad ve konum kullanarak bir kaynak grubu oluşturabilir ve ardından kaynak grubuna eklemek üzere kaynak oluşturmak için New-AzureRmResource cmdlet 'ini kullanabilirsiniz.
Var olan bir kaynak grubuna dağıtım eklemek için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın. Var olan kaynak grubuna kaynak eklemek için, **New-AzureRmResource** cmdlet 'ini kullanın. Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir. Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.

## ÖRNEKLERDEN

### Örnek 1: boş bir kaynak grubu oluşturma
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

Bu komut, kaynağı olmayan bir kaynak grubu oluşturur. Bu kaynak grubuna kaynak ve dağıtım eklemek için **New-azurermresource** veya **New-AzureRmResourceGroupDeployment** cmdlet 'lerini kullanabilirsiniz.

### Örnek 2: konum parametrelerini kullanarak boş bir kaynak grubu oluşturma
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

Bu komut, kaynağı olmayan bir kaynak grubu oluşturur.

### Örnek 3: etiketlerle kaynak grubu oluşturma
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Bu komut boş bir kaynak grubu oluşturur. Bu komut, örnek 1 ' deki komutla aynı olur; bunun nedeni kaynak grubuna Etiketler atar. Boş adlı ilk etiket, kaynağı olmayan kaynak gruplarını belirlemek için kullanılabilir. İkinci etiket bölümlendirilir ve bir pazarlama değeri içerir. Yönetim veya bütçeleme için kaynak gruplarını sınıflandırmak için bu gibi bir etiket kullanabilirsiniz.

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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Konum
Kaynak grubunun konumunu belirtir. Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu belirtin. Herhangi bir konuma kaynak grubu yerleştirebilirsiniz. Kaynak grubunun Azure aboneliğinizde aynı konumda veya kaynaklarıyla aynı konumda olması gerekmez.
Hangi konumun kaynak türlerini desteklediğini belirlemek için Get-AzureRmResourceProvider cmdlet 'ini *Providernamespace* parametresiyle kullanın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Kaynak grubu için bir ad belirtir. Kaynak adı abonelikte benzersiz olmalıdır. Bu ada sahip bir kaynak grubu zaten varsa, komut varolan kaynak grubunu değiştirmeden önce sizden onay sorar.

```yaml
Type: System.String
Parameter Sets: (All)
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
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} etiket eklemek veya değiştirmek Için, kaynak grubunun etiket koleksiyonunu değiştirmelisiniz.
Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzureRmResource ve Get-AzureRmResourceGroup *Etiket parametresini kullanarak* etiket adına veya ad ve değere göre arama yapabilirsiniz. Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.
Önceden tanımlanmış etiketleri almak için Get-AzureRMTag cmdlet 'ini kullanın.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
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

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManagement. modeller. PSResourceGroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Yeni-AzureRmResource](./New-AzureRmResource.md)

[Yeni-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)
