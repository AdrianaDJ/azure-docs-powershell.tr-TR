---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279807"
---
# Set-AzRoleDefinition

## SYNOPSIS
Azure RBAC 'de özel bir rolü değiştirir.
Değiştirilmiş rol tanımını JSON dosyası veya PSRoleDefinition olarak sağlayın.
İlk olarak, değiştirmek istediğiniz özel rolü almak için Get-AzRoleDefinition komutunu kullanın.
Ardından, değiştirmek istediğiniz özellikleri değiştirin.
Son olarak bu komutu kullanarak rol tanımını kaydedin.

## INDEKI

### Inputfileparameterset
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Set-AzRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde var olan bir özel rolü güncelleştirir.
Güncelleştirilmiş rol tanımını, bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.
Güncelleştirilmiş özel rolün rol tanımı, güncelleştirilmese bile, rolün kimliğini ve tüm diğer gerekli özelliklerini içermelidir: DisplayName, Description, Actions, Astifblescopes.
NotActions, DataActions, NotDataActions isteğe bağlıdır.
Aşağıda, Set-AzRoleDefinition {"ID": "için güncelleştirilmiş bir rol tanımı JSON 'si verilmiştir 52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "güncelleştirilmiş rol", "Açıklama": "tüm kaynakları izleyebilir ve sanal makineleri başlatıp yeniden başlatabilirsiniz", "eylemler": \[ " */Read", "Microsoft. Classıntericcompute/virtualmachines/restart/Action", "Microsoft. Classıntericcompute/virtualmachines/start/ACTION" \] , "NotActions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Read" \] , "Notdataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Write" \] , "astifblescopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## ÖRNEKLERDEN

### Örnek 1: PSRoleDefinitionObject kullanarak güncelleştir
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Örnek 2: JSON dosyası kullanarak oluşturma
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRELERINE

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

### -GirdiDosyası
Güncelleştirilecek tek bir JSON rol tanımı içeren dosya adı.
Yalnızca JSON 'de güncelleştirilecek özellikleri ekleyin.
ID özelliği gereklidir.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Güncelleştirilecek rol tanımı nesnesi

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-Azroltanımı](./Get-AzRoleDefinition.md)

[Yeni-Azrol tanımı](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

