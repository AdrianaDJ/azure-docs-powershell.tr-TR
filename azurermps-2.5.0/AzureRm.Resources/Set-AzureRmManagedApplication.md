---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 8fb6c2d299799849d1e9f2183621e9fc31cc0acd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939047"
---
# Set-AzureRmManagedApplication

## SYNOPSIS
Yönetilen uygulamayı güncelleştirir

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Setbynaik Vseçresourcegroup (varsayılan)
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Setbyıd
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamaları güncelleştirir

## ÖRNEKLERDEN

### Örnek 1: yönetilen uygulama tanımı açıklamasını güncelleştirme
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

Bu komut, yönetilen uygulama açıklamasını güncelleştirir

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
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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
Abonelik dahil, tam nitelikli yönetilen uygulama kimliği. Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tür
Yönetilen uygulama türü.
Market veya servicecatalog 'tan biri

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

### -Managedapplicationdefinitionıd
Yönetilen kaynak grubu adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedResourceGroupName
Yönetilen kaynak grubu adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Yönetilen uygulama adı.

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parametre
Yönetilen uygulama için JSON biçimli parametrelerin dizesi.
Bu, parametre içeren bir dosya adı veya URI veya parametre olarak parametre yolu olabilir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Yönetilen uygulama planı özelliklerini temsil eden karma bir tablo.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketlerini temsil eden karma bir tablo.

```yaml
Type: Hashtable
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
System. topluluklar. Hashtable

## ÇıKıŞLAR

### System. Management. Automation. PSObject

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
