---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592906"
---
# Get-AzureRmPolicySetDefinition

## SYNOPSIS
İlke kümesi tanımlarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### GetBySubscription (varsayılan)
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Getbynaik Vseçresourcegroup
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetById
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmPolicySetDefinition** cmdlet 'i, tüm ilke kümesi tanımlarını veya ad veya kimlikle tanımlanan belirli bir ilke kümesi tanımını alır.

## ÖRNEKLERDEN

### Örnek 1: tüm ilke kümesi tanımını alma
```
PS C:\>Get-AzureRmPolicySetDefinition
```

Bu komut, tüm ilke kümesi tanımlarını alır.

### Örnek 2: ada göre ilke kümesi tanımını alma
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

Bu komut, VMPolicyDefinition adındaki ilke kümesi tanımını alır.

## PARAMETRELERINE

### -Apıversion
Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.
Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.
Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
İlke kümesi tanım adı.

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre-
Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. Management. Automation. PSObject

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
