---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: c6dd17917624d8b2b914ac94c8310358fac03b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592904"
---
# Get-AzureRmRoleAssignment

## SYNOPSIS
Belirtilen kapsamda Azure RBAC rol atamalarını listeler.
Varsayılan olarak, seçilen Azure aboneliğindeki tüm rol atamalarını listeler.
Belirli bir kullanıcıya yönelik atamaları listelemek veya belirli bir kaynak grubundaki veya kaynağındaki atamaları listelemek için ilgili parametreleri kullanın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### EmptyParameterSet (varsayılan)
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NesneKimliği
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourcegroupwithobjectivseçparameterset
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourcewithobjectivseçparameterset
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Scopewithobjectivseçparameterset
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Roleıdwithscopeandobjectivseçparameterset
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SignInNameParameterSet
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupParameterSet
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceParameterSet
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeParameterSet
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Kapsamda etkili olan tüm rol atamalarını listelemek için Get-AzureRMRoleAssignment komutunu kullanın.

Parametre olmadan bu komut, aboneliğin altında yapılan tüm rol atamalarını döndürür.
Bu listeye, sorumlu, rol ve kapsam için filtreleme parametrelerini kullanarak filtre uygulanabilir.

Atamanın konusu belirtilmelidir.
Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.
Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.
Bir Azure AD uygulaması belirtmek için, ServicePrincipalName veya ObjectID parametrelerini kullanın.

Atanmış olan rolün, RoleDefinitionName parametresi kullanılarak belirtilmesi gerekir.

Erişimin verildiği kapsam belirtilebilir.
Varsayılan olarak seçili aboneliği alır. Atamanın kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.
Kapsam-bu,/Subscriptions/ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .
Bu, söz konusu kapsamda geçerli olan atamalara filtre uygulanır Yani, bu kapsamda ve yukarıdaki tüm atamalar.
ib.
ResourceGroupName-aboneliğin altındaki herhangi bir kaynak grubunun adı.
Bu, atamaların belirtilen c kaynak grubunda geçerli olduğunu filtreedecektir.
ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-aboneliğin altındaki belirli bir kaynağı tanımlar ve bu kaynak kapsamında atamaları geçerli filtreedecektir.

Belirli bir kullanıcının abonelikteki erişimi belirlemek için, ExpandPrincipalGroups anahtarını kullanın.
Kullanıcıya atanan tüm roller ve kullanıcının üyesi olduğu gruplar listelenir.

Ayrıca, abonelik yöneticilerini ve ortak yöneticileri de görüntülemek için ıncludeclassıntericadministrators anahtarını kullanın.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmRoleAssignment
```

Abonelikteki tüm rol atamalarını listeleme

### Örnek 2
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

Kullanıcıya yapılan tüm rol atamalarını john.doe@contoso.com ve üye olduğu grupları, testRG kapsamındaki veya üstünde alır.

### Örnek 3
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

Belirtilen hizmet sorumlusunun tüm rol atamalarını alır

### Örnek 4
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

' Site1 ' Web sitesi kapsamındaki rol atamalarını alır.

## PARAMETRELERINE

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

### -ExpandPrincipalGroups
Belirtilmişse, doğrudan kullanıcıya atanan rolleri ve kullanıcının üyesi olduğu grupları döndürür (geçişli).
Yalnızca Kullanıcı sorumlusu için desteklenir.

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Includeclassıntericadministrators
Belirtilmişse, abonelik klasik yöneticileri (ortak yönetici, hizmet yöneticileri vb.) rol atamalarını da listeler.

```yaml
Type: SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectID
Kullanıcının, grubun veya hizmetin Azure AD ObjectID.
Belirtilen sorumluya yapılan tüm atamalara filtre uygular.

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
ResourceName parametresi kullanılarak belirtilen kaynak hiyerarşisindeki üst kaynak.
ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.
Belirtilen kaynak grubunda geçerli olan rol atamalarını listeler.
ResourceName, ResourceType ve ParentResource parametreleriyle birlikte kullanıldığında, komut, atamaları kaynak grubundaki kaynaklar için geçerli listeler.

```yaml
Type: String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Kaynak adı.
Örneğin, storageaccountprod.
ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Kaynak türü.
Örneğin, Microsoft. Network/virtualNetworks.
ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Roledefinitionıd
Sorumluya atanmış olan rolün kimliği.

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionName
Kullanıcıya atanan rol (Reader, katılımcı, sanal ağ yöneticisi vb.).

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kapsam
Rol atamasının kapsamı.
Göreli URI biçiminde.
Örneğin,/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg.
"/Subscriptions/{id}" ile başlamalıdır.
Komut bu kapsamda geçerli olan tüm atamalara filtre uygular.

```yaml
Type: String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Hizmet sorumlusunun ServicePrincipalName.
Belirtilen Azure AD uygulamasına yapılan tüm atamalara filtre uygular.

```yaml
Type: String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Signınname
Kullanıcının e-posta adresi veya Kullanıcı asıl adı.
Belirtilen kullanıcıya yapılan tüm atamalara filtre uygular.

```yaml
Type: String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev]

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Yeni-Azurermroleataması](./New-AzureRmRoleAssignment.md)

[Remove-Azurermroleataması](./Remove-AzureRmRoleAssignment.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

