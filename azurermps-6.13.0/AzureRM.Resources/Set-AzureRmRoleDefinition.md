---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: f0c22f199d19e97f957bc86fbee8d649d30b622d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764295"
---
# Set-AzureRmRoleDefinition

## SYNOPSIS
Azure RBAC 'de özel bir rolü değiştirir.
Değiştirilmiş rol tanımını JSON dosyası veya PSRoleDefinition olarak sağlayın.
İlk olarak, değiştirmek istediğiniz özel rolü almak için Get-AzureRmRoleDefinition komutunu kullanın.
Ardından, değiştirmek istediğiniz özellikleri değiştirin.
Son olarak bu komutu kullanarak rol tanımını kaydedin.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Inputfileparameterset
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Set-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde var olan bir özel rolü güncelleştirir.
Güncelleştirilmiş rol tanımını, bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.
Güncelleştirilmiş özel rolün rol tanımı, güncelleştirilmese bile, rolün kimliğini ve tüm diğer gerekli özelliklerini içermelidir: DisplayName, Description, Actions, Astifblescopes.
NotActions, DataActions, NotDataActions isteğe bağlıdır.
Aşağıda, Set-AzureRmRoleDefinition {"ID": "için güncelleştirilmiş bir rol tanımı JSON 'si verilmiştir 52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "güncelleştirilmiş rol", "Açıklama": "tüm kaynakları izleyebilir ve sanal makineleri başlatıp yeniden başlatabilirsiniz", "eylemler": \[ " */Read", "Microsoft. Classıntericcompute/virtualmachines/restart/Action", "Microsoft. Classıntericcompute/virtualmachines/start/ACTION" \] , "NotActions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Read" \] , "Notdataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Write" \] , "astifblescopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## ÖRNEKLERDEN

### PSRoleDefinitionObject kullanarak güncelleştir
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### JSON dosyası kullanarak oluştur
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRELERINE

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition
Parametreler: rol (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Yeni-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

