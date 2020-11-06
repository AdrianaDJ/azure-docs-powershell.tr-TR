---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592571"
---
# New-AzureRmResourceGroupDeployment

## SYNOPSIS
Kaynak grubuna Azure dağıtımı ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Parametre olmadan şablon dosyasıyla dağıtım (varsayılan)
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Şablon dosyası ve şablon parametreleri nesnesi aracılığıyla dağıtım
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Şablon URI ve şablon parametreleri nesnesi aracılığıyla dağıtım
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Şablon dosyası ve şablon parametreleri dosyasıyla dağıtım
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Şablon URI 'si ve şablon parametreleri dosyasıyla dağıtım
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Şablon dosyası şablonu
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Şablon URI 'si ve şablon parametreleri URI 'si aracılığıyla dağıtım
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Parametre olmadan şablon URI ile dağıtım
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmResourceGroupDeployment** cmdlet 'i var olan bir kaynak grubuna dağıtım ekler.
Bu, dağıtımın gerektirdiği kaynakları içerir.

Azure kaynağı, veritabanı sunucusu, veritabanı, Web sitesi, sanal makine veya depolama hesabı gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.
Bir Azure Kaynak grubu, Web sitesi, veritabanı sunucusu ve finansal web sitesi için gerekli veritabanları gibi bir birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.
Kaynak grubu dağıtımı, kaynak grubuna kaynak eklemek için şablon kullanır ve bunları Azure 'da kullanılabilir olacak şekilde yayımlar.
Kaynak grubuna şablon kullanmadan kaynak eklemek için New-AzureRmResource cmdlet 'ini kullanın.

Kaynak grubu dağıtımı eklemek için, varolan bir kaynak grubunun adını ve bir kaynak grup şablonunu belirtin.
Kaynak grubu şablonu, Web portalı gibi karmaşık bir bulut tabanlı hizmetin kaynak grubunu temsil eden bir JSON dizesidir.
Şablonda, gerekli kaynaklar ve adları ve boyutları gibi yapılandırılabilir özellik değerlerini içeren parametre yer tutucuları vardır.
Azure şablon galerisinde birçok şablon bulabilir veya kendi şablonlarınızı oluşturabilirsiniz.
Galeride bir şablon bulmak için **Get-Azurermresourcegroupgallertemplate** cmdlet 'ini kullanabilirsiniz.

Kaynak grubu oluşturmak üzere özel bir şablon kullanmak için, *TemplateFile* parametresini veya *templateuri* parametresini belirtin.
Her şablonda, yapılandırılabilir özellikler için parametreler vardır.
Şablon parametrelerinin değerlerini belirtmek için, *Templateparameterfıle* parametresini veya *templateparameternesne* parametresini belirtin.
Alternatif olarak, bir şablon belirttiğinizde komuta dinamik olarak eklenen şablon parametrelerini de kullanabilirsiniz.
Dinamik parametreleri kullanmak için, bunları komut istemine yazın veya parametre belirtmek için eksi işareti (-) girin ve kullanılabilir parametreler arasında geçiş yapmak için sekme tuşunu kullanın.
Komut istemine girdiğiniz şablon parametre değerleri, bir şablon parametre nesnesi veya dosyasındaki değerlerden önceliklidir.

## ÖRNEKLERDEN

### Örnek 1: dağıtım oluşturmak için özel bir şablon ve parametre dosyası kullanma
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

Bu komut, özel bir şablon ve diskte bir şablon dosyası kullanarak yeni bir dağıtım oluşturur.
Bu komut, parametre ve parametre değerleri içeren bir dosyayı belirtmek için şablonu ve *Templateparameterfile* parametresini belirtmek üzere *TemplateFile* parametresini kullanır.
Şablonun sürümünü belirtmek için *Templateversion* parametresini kullanır.

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

### -DeploymentDebugLogLevel
Bir hata ayıklama günlüğü düzeyi belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- RequestContent 
- ResponseContent 
- Tüm 
- Yabilirsiniz

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Mod
Dağıtım modunu belirtir. Bu parametre için kabul edilebilir değerler şunlardır:

- Tamamlamanıza 
- Numarasında

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Oluşturulacak kaynak grubu dağıtımının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
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

### -ResourceGroupName
Dağıtılacak kaynak grubunun adını belirtir.

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

### -TemplateFile
JSON şablon dosyasının tam yolunu belirtir.
Bu, özel bir şablon veya bir JSON dosyası olarak kaydedilmiş, **-Azurermresourcegroupgallertemplate** cmdlet 'i kullanılarak oluşturulmuş bir galeri şablonu olabilir.

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterFile
Şablon parametrelerinin adlarını ve değerlerini içeren bir JSON dosyasının tam yolunu belirtir.
Şablonda parametreler varsa, parametre değerlerini *Templateparameterfile* parametresiyle veya *templateparameterobject* parametresiyle belirtmeniz gerekir.
Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.

Dinamik parametreleri kullanmak için, parametre adını belirtmek üzere eksi işareti (-) yazın ve ardından kullanılabilir parametrelerde gezinmek için sekme tuşunu kullanın.

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterObject
Şablon parametre adları ve değerlerinin karma tablosunu belirtir.
Windows PowerShell 'de karma tablolarla ilgili yardım için, yazın `Get-Help about_Hash_Tables` .
Şablonda parametreler varsa, parametre değerleri belirtmeniz gerekir.
Şablon belirttiğinizde, şablon parametreleri komuta dinamik olarak eklenir.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterUri
Şablon parametreleri dosyasının URI 'sini belirtir.

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateUri
JSON şablon dosyasının URI 'sini belirtir.
Bu dosya, özel bir şablon veya **Kaydet-Azurermresourcegroupgallertemplate** gıbı bir JSON dosyası olarak kaydedilmiş bir galeri şablonu olabilir.

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. model. PSResourceGroupDeployment

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmResourceGroupDeployment](./Get-AzureRmResourceGroupDeployment.md)

[Yeni-AzureRmResource](./New-AzureRmResource.md)

[Yeni-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Stop-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


