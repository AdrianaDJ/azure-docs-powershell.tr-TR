---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592903"
---
# Get-AzureRmRoleDefinition

## SYNOPSIS
Ödev için kullanılabilen tüm Azure RBAC rollerini listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### RoleDefinitionNameParameterSet
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Roledefinitionıdparameterset
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Ayrıntılarını görüntülemek için Get-AzureRmRoleDefinition komutunu belirli bir rol adıyla birlikte kullanın.
Rolün erişim verdiği tek tek işlemleri denetlemek için, rolün eylemlerini ve NotActions özelliklerini gözden geçirin.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

Okuyucu rol tanımını alma

### Örnek 2
```
PS C:\> Get-AzureRmRoleDefinition
```

Tüm RBAC rol tanımlarını listeler

## PARAMETRELERINE

### -AtScopeAndBelow
Belirtilmişse, tüm rol tanımlarını görüntüler.

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Özel
Belirtilmişse, yalnızca dizindeki özel oluşturulmuş rolleri görüntüler.

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Rol tanımı kimliği.

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Rol tanımı adı.
Örneğin, okuyucu, katılımcı, sanal makine katılımcısı.

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kapsam
Rol tanımı kapsamı.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Dizisi
' Scope ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition]

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Yeni-Azurermroleataması](./New-AzureRmRoleAssignment.md)

[Get-Azurermroleödev](./Get-AzureRmRoleAssignment.md)

[Yeni-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

