---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108055"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
Kaynak grubundaki dağıtımları alır.

## INDEKI

### GetByResourceGroupDeploymentName (varsayılan)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubunda dağıtımları alır.
Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.
Varsayılan olarak **Get-AzResourceGroupDeployment** belirtilen bir kaynak grubunun tüm dağıtımlarını alır.
Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.
Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.
Dağıtım, kaynak grubundaki kaynakların kullanılabilmesini sağlayan bir işlemdir.
Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzResourceGroup cmdlet 'ine bakın.
Bu cmdlet 'i izleme için kullanabilirsiniz.
Hata ayıklama için, bu cmdlet 'i Get-AzLog cmdlet ile kullanın.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubu için tüm dağıtımları alma
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Bu komut, ContosoLabsRG kaynak grubu için tüm dağıtımları alır.
Çıktıda, Galeri şablonu kullanan bir WordPress blogu için dağıtım gösterilir.

### Örnek 2: ada göre dağıtım alma
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Bu komut, ContosoLabsRG kaynak grubunun DeployWebsite01 dağıtımını alır.
**Yeni-AzResourceGroup** veya **New-AzResourceGroupDeployment** cmdlet 'lerini kullanarak bir dağıtıma bir ad atayabilirsiniz.
Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.

### Örnek 3: tüm kaynak gruplarının dağıtımlarını alma
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Bu komut, Get-AzResourceGroup cmdlet 'ini kullanarak aboneliğinizdeki tüm kaynak gruplarını alır.
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
Alınacak kaynak grubu dağıtımının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
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
Parameter Sets: GetByResourceGroupDeploymentName
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
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroupDeployment

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[Yeni-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


