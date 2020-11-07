---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 25f0227cad9299de8a04d0bfcfde16e9728dcc7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759371"
---
# New-AzRoleDefinition

## SYNOPSIS
Azure RBAC 'de özel bir rol oluşturur.
Giriş olarak bir JSON rol tanımı dosyası veya PSRoleDefinition nesnesi sağlayın.
İlk olarak, temel rol tanımı nesnesi oluşturmak için Get-AzRoleDefinition komutunu kullanın.
Ardından özelliklerini gerektiği gibi değiştirin.
Son olarak, rol tanımını kullanarak özel bir rol oluşturmak için bu komutu kullanın.

## INDEKI

### Inputfileparameterset
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
New-AzRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol oluşturur.
Bir rol tanımını bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.
Giriş rol tanımında aşağıdaki özellikler bulunmalıdır:
1) DisplayName: özel rolün adı
2) Açıklama: rolün verdiği erişimi özetleyen rolün kısa bir açıklaması.
3) Eylemler: özel rolün erişim verdiği işlemler kümesi.
Azure RBAC kullanılarak güvenliği sağlansağlanan Azure Kaynak sağlayıcılarının işlemini edinmek için Get-AzProviderOperation kullanın.
Aşağıda bazı geçerli işlem dizeleri verilmiştir:
 - "*/Read" tüm Azure Resource sağlayıcılarının okuma işlemlerine erişim verir.
 - "Microsoft. Network/*/Read" Azure 'un Microsoft. Network Resource Provider 'daki tüm kaynak türlerinin okuma işlemlerine erişim sağlar.
 - "Microsoft. COMPUTE/virtualMachines/*" sanal makinelerin tüm işlemlerine ve alt kaynak türlerine erişim sağlar.
4) Astabeblescopes: özel rolün atama için kullanılabileceği kapsam kümesi (Azure abonelikleri veya kaynak grupları).
Astifblescopes 'ı kullanarak, özel rolü yalnızca gerekli olan aboneliklere veya kaynak gruplarında kullanılabilir hale getirebilirsiniz ve aboneliğin veya kaynak gruplarının geri kalanı için Kullanıcı deneyimini ikincil haline getirebilirsiniz.
Aşağıdakiler geçerli atanabilir kapsamlardır:
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rolün iki abonelikteki ödev için kullanılabilir olmasını sağlar.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": rolün tek bir abonelikte ödev için kullanılabilir olmasını sağlar.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rolün yalnızca ağ kaynak grubundaki ödev için kullanılabilir olmasını sağlar.
Giriş rol tanımı aşağıdaki özellikleri içerebilir:
1) NotActions: özel rolün etkili eylemlerini belirlemek için eylemlerin dışında tutulması gereken işlemler kümesi.
Özel bir rolde erişim vermek istemediğiniz belirli bir işlem varsa, bu belirli işlemler yerine bu belirli işlemler dışında tüm işlemleri belirtmek yerine NotActions 'ı kullanmak uygun olacaktır.
2) DataActions: özel rolün erişim verdiği veri işlemleri kümesi.
3) Notvereylemler: özel rolün etkin veri eylemlerini belirlemek için DataActions 'tan dışlanması gereken işlemler kümesi.
Özel bir rolde erişim vermek istemediğiniz belirli bir veri işlemi varsa, eylemlerdeki belirli işlemler dışında tüm işlemleri yerine çıkarmak için NotDataActions 'ı kullanmak kullanışlıdır.
Not: kullanıcıya, NotActions 'da bir işlemi belirten bir rol atanmışsa ve başka bir rolün aynı işleme erişim izni verdiğini düşünüyorsanız, Kullanıcı bu işlemi gerçekleştirebilir.
NotActions, bir Reddedilenler kuralı değil; belirli işlemler dışlanmak gerektiğinde izin verilen işlemler kümesi oluşturmanın kullanışlı bir yoludur.
Aşağıda, giriş {"ad": "güncelleştirilen rol", "Açıklama": "tüm kaynakları izleyebilir,", "eylemler": \[ " */Read", "Microsoft. Classıntericcompute/virtualmachines/restart/Action", "Microsoft. classıntericcompute/virtualmachines/restart/Action" \] , "NotActions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Read" \] , "Notdataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Write" \] \[ \]

## ÖRNEKLERDEN

### PSRoleDefinitionObject kullanarak oluşturma
```
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"
          PS C:\> $role.Id = $null
          PS C:\> $role.Name = "Virtual Machine Operator"
          PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
          PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
          PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
          PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
          PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
          PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
          PS C:\> $role.Actions.Add("Microsoft.Support/*")
          PS C:\> $role.AssignableScopes.Clear()
          PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> New-AzRoleDefinition -Role $role
```

### JSON dosyası kullanarak oluştur
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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
Tek bir JSON rol tanımını içeren dosya adı.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Rol tanımı nesnesi.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-Azroltanımı](./Get-AzRoleDefinition.md)

[Set-Azroltanımı](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

