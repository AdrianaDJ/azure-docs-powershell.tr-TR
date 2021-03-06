---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322954"
---
# Get-AzResourceGroup

## SYNOPSIS
Kaynak gruplarını alır.

## INDEKI

### GetByResourceGroupName (varsayılan)
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyresourcegroupıd
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzResourceGroup** cmdlet 'i geçerli abonelikteki Azure kaynak gruplarını alır.
Tüm kaynak gruplarını alabilir veya bir kaynak grubunu ada veya başka özelliklere göre belirtebilirsiniz.
Varsayılan olarak, bu cmdlet geçerli abonelikteki tüm kaynak gruplarını alır.
Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzResourceGroup cmdlet 'ine bakın.

## ÖRNEKLERDEN

### Örnek 1: ada göre kaynak grubu alma
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

Bu komut, Kurerblogu adlı aboneliğinizdeki Azure kaynak grubunu alır.

### Örnek 2: kaynak grubunun tüm etiketlerini alma
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Bu komut ContosoRG adındaki kaynak grubunu alır ve bu grupla ilişkilendirilmiş etiketleri görüntüler.

### Örnek 3: etikete dayalı kaynak gruplarını alma
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### Örnek 4: konuma göre kaynak gruplarını gösterme
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Örnek 5: belirli bir konumdaki tüm kaynak gruplarının adlarını gösterme
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Örnek 6: adları WebSunucusu ile başlayan kaynak gruplarını göster
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

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
Alınacak kaynak grubunun KIMLIĞINI belirtir.
Joker karakterler kullanılamaz.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Alınacak kaynak grubunun konumunu belirtir.

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

### -Ad
Alınacak kaynak grubunun adını belirtir. Bu parametre, dizenin başında ve/veya sonunda joker karakterleri destekler.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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
Kaynak gruplarını filtreleme

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)

