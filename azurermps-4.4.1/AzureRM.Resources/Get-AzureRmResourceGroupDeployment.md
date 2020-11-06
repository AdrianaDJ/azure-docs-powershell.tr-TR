---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592578"
---
# Get-AzureRmResourceGroupDeployment

## SYNOPSIS
Kaynak grubundaki dağıtımları alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Dağıtım adı parametre kümesi. Varsayýlan
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Dağıtım kimliği parametre kümesi.
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubunda dağıtımları alır.
Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.
Varsayılan olarak **Get-AzureRmResourceGroupDeployment** belirtilen bir kaynak grubu için tüm dağıtımları alır.

Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.
Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.

Dağıtım, kaynak grubundaki kaynakların kullanılabilmesini sağlayan bir işlemdir.
Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzureRmResourceGroup cmdlet 'ine bakın.

Bu cmdlet 'i izleme için kullanabilirsiniz.
Hata ayıklama için, bu cmdlet 'i Get-AzureRmLog cmdlet ile kullanın.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubu için tüm dağıtımları alma
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Bu komut, ContosoLabsRG kaynak grubu için tüm dağıtımları alır.
Çıktıda, Galeri şablonu kullanan bir WordPress blogu için dağıtım gösterilir.

### Örnek 2: ada göre dağıtım alma
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Bu komut, ContosoLabsRG kaynak grubunun DeployWebsite01 dağıtımını alır.
**Yeni-AzureRmResourceGroup** veya **New-AzureRmResourceGroupDeployment** cmdlet 'lerini kullanarak bir dağıtıma bir ad atayabilirsiniz.
Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.

### Örnek 3: tüm kaynak gruplarının dağıtımlarını alma
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Bu komut, Get-AzureRmResourceGroup cmdlet 'ini kullanarak aboneliğinizdeki tüm kaynak gruplarını alır.
Komut, ardışık düzen işlecini kullanarak kaynak gruplarını geçerli cmdlet 'e geçirir.
Geçerli cmdlet, abonelikteki tüm kaynak gruplarının tüm dağıtımlarını alır ve onları **Resourcegroupname** , **DeploymentName** ve **provisioningstate** özellik değerlerini görüntülemek için Format-Table cmdlet 'ine geçirir.

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

### -ID
Alınacak kaynak grubu dağıtımının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak dağıtımın adını belirtir.
Joker karakterler kullanılamaz.

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
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
Kaynak grubunun adını belirtir.
Cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımlarını alır.
Joker karakterler kullanılamaz.
Bu parametre gereklidir ve her komutta yalnızca bir kaynak grubu belirtebilirsiniz.

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. ResourceManagement. modeller. PSResourceGroupDeployment
Cmdlet kaynak grubu dağıtımlarını döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Yeni-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Yeni-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Stop-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


