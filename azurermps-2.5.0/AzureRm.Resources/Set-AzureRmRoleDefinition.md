---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939463"
---
# <span data-ttu-id="d9336-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9336-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="d9336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9336-102">SYNOPSIS</span></span>
<span data-ttu-id="d9336-103">Azure RBAC 'de özel bir rolü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d9336-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="d9336-104">Değiştirilmiş rol tanımını JSON dosyası veya PSRoleDefinition olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="d9336-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="d9336-105">İlk olarak, değiştirmek istediğiniz özel rolü almak için Get-AzureRmRoleDefinition komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="d9336-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="d9336-106">Ardından, değiştirmek istediğiniz özellikleri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d9336-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="d9336-107">Son olarak bu komutu kullanarak rol tanımını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="d9336-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9336-108">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9336-108">SYNTAX</span></span>

### <span data-ttu-id="d9336-109">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="d9336-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9336-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9336-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9336-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9336-111">DESCRIPTION</span></span>
<span data-ttu-id="d9336-112">Set-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde var olan bir özel rolü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d9336-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="d9336-113">Güncelleştirilmiş rol tanımını, bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="d9336-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="d9336-114">Güncelleştirilmiş özel rolün rol tanımı, güncelleştirilmese bile, rolün kimliğini ve tüm diğer gerekli özelliklerini içermelidir: DisplayName, Description, Actions, Astifblescopes.</span><span class="sxs-lookup"><span data-stu-id="d9336-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="d9336-115">NotActions, DataActions, NotDataActions isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d9336-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="d9336-116">Aşağıda, Set-AzureRmRoleDefinition {"ID": "için güncelleştirilmiş bir rol tanımı JSON 'si verilmiştir 52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "güncelleştirilmiş rol", "Açıklama": "tüm kaynakları izleyebilir ve sanal makineleri başlatıp yeniden başlatabilirsiniz", "eylemler": \[ " */Read", "Microsoft. Classıntericcompute/virtualmachines/restart/Action", "Microsoft. Classıntericcompute/virtualmachines/start/ACTION" \] , "NotActions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Read" \] , "Notdataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Write" \] , "astifblescopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="d9336-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="d9336-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9336-117">EXAMPLES</span></span>

### <span data-ttu-id="d9336-118">PSRoleDefinitionObject kullanarak güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d9336-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="d9336-119">JSON dosyası kullanarak oluştur</span><span class="sxs-lookup"><span data-stu-id="d9336-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="d9336-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9336-120">PARAMETERS</span></span>

### <span data-ttu-id="d9336-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9336-121">-DefaultProfile</span></span>
<span data-ttu-id="d9336-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9336-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9336-123">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="d9336-123">-InputFile</span></span>
<span data-ttu-id="d9336-124">Güncelleştirilecek tek bir JSON rol tanımı içeren dosya adı.</span><span class="sxs-lookup"><span data-stu-id="d9336-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="d9336-125">Yalnızca JSON 'de güncelleştirilecek özellikleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d9336-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="d9336-126">ID özelliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d9336-126">Id property is Required.</span></span>

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

### <span data-ttu-id="d9336-127">-Role</span><span class="sxs-lookup"><span data-stu-id="d9336-127">-Role</span></span>
<span data-ttu-id="d9336-128">Güncelleştirilecek rol tanımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d9336-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="d9336-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9336-129">CommonParameters</span></span>
<span data-ttu-id="d9336-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9336-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9336-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9336-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9336-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9336-132">INPUTS</span></span>

### <span data-ttu-id="d9336-133">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9336-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="d9336-134">Parametreler: rol (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9336-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="d9336-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9336-135">OUTPUTS</span></span>

### <span data-ttu-id="d9336-136">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9336-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="d9336-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9336-137">NOTES</span></span>
<span data-ttu-id="d9336-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="d9336-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d9336-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9336-139">RELATED LINKS</span></span>

[<span data-ttu-id="d9336-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d9336-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="d9336-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9336-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="d9336-142">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9336-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="d9336-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9336-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

