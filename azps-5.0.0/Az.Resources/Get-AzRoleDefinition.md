---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322906"
---
# Get-AzRoleDefinition

## SYNOPSIS
Ödev için kullanılabilen tüm Azure RBAC rollerini listeler.

## INDEKI

### RoleDefinitionNameParameterSet (varsayılan)
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Roledefinitionıdparameterset
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Ayrıntılarını görüntülemek için Get-AzRoleDefinition komutunu belirli bir rol adıyla birlikte kullanın.
Rolün erişim verdiği tek tek işlemleri denetlemek için, rolün eylemlerini ve NotActions özelliklerini gözden geçirin.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

Okuyucu rol tanımını alma

### Örnek 2
```
PS C:\> Get-AzRoleDefinition
```

Tüm RBAC rol tanımlarını listeler

## PARAMETRELERINE

### -Özel
Belirtilmişse, yalnızca dizindeki özel oluşturulmuş rolleri görüntüler.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Rol tanımı kimliği.

```yaml
Type: System.Guid
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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Guid

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Yeni-Azrol ataması](./New-AzRoleAssignment.md)

[Get-Azrol ataması](./Get-AzRoleAssignment.md)

[Yeni-Azrol tanımı](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

