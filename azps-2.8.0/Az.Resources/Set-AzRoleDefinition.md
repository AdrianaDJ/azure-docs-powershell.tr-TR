---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 0ea0c0345bc57a7b1bd5c0c4cf67d6bd400542be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933293"
---
# <span data-ttu-id="94408-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="94408-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="94408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94408-102">SYNOPSIS</span></span>
<span data-ttu-id="94408-103">Azure RBAC 'de özel bir rolü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="94408-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="94408-104">Değiştirilmiş rol tanımını JSON dosyası veya PSRoleDefinition olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="94408-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="94408-105">İlk olarak, değiştirmek istediğiniz özel rolü almak için Get-AzRoleDefinition komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="94408-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="94408-106">Ardından, değiştirmek istediğiniz özellikleri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="94408-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="94408-107">Son olarak bu komutu kullanarak rol tanımını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="94408-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="94408-108">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94408-108">SYNTAX</span></span>

### <span data-ttu-id="94408-109">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="94408-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94408-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="94408-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94408-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="94408-111">DESCRIPTION</span></span>
<span data-ttu-id="94408-112">Set-AzRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde var olan bir özel rolü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="94408-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="94408-113">Güncelleştirilmiş rol tanımını, bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="94408-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="94408-114">Güncelleştirilmiş özel rolün rol tanımı, güncelleştirilmese bile, rolün kimliğini ve tüm diğer gerekli özelliklerini içermelidir: DisplayName, Description, Actions, Astifblescopes.</span><span class="sxs-lookup"><span data-stu-id="94408-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="94408-115">NotActions, DataActions, NotDataActions isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="94408-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="94408-116">Aşağıda, Set-AzRoleDefinition {"ID": "için güncelleştirilmiş bir rol tanımı JSON 'si verilmiştir 52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "güncelleştirilmiş rol", "Açıklama": "tüm kaynakları izleyebilir ve sanal makineleri başlatıp yeniden başlatabilirsiniz", "eylemler": \[ " */Read", "Microsoft. Classıntericcompute/virtualmachines/restart/Action", "Microsoft. Classıntericcompute/virtualmachines/start/ACTION" \] , "NotActions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Read" \] , "Notdataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Write" \] , "astifblescopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="94408-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="94408-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94408-117">EXAMPLES</span></span>

### <span data-ttu-id="94408-118">PSRoleDefinitionObject kullanarak güncelleştir</span><span class="sxs-lookup"><span data-stu-id="94408-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="94408-119">JSON dosyası kullanarak oluştur</span><span class="sxs-lookup"><span data-stu-id="94408-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="94408-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94408-120">PARAMETERS</span></span>

### <span data-ttu-id="94408-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94408-121">-DefaultProfile</span></span>
<span data-ttu-id="94408-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="94408-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94408-123">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="94408-123">-InputFile</span></span>
<span data-ttu-id="94408-124">Güncelleştirilecek tek bir JSON rol tanımı içeren dosya adı.</span><span class="sxs-lookup"><span data-stu-id="94408-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="94408-125">Yalnızca JSON 'de güncelleştirilecek özellikleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="94408-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="94408-126">ID özelliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="94408-126">Id property is Required.</span></span>

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

### <span data-ttu-id="94408-127">-Role</span><span class="sxs-lookup"><span data-stu-id="94408-127">-Role</span></span>
<span data-ttu-id="94408-128">Güncelleştirilecek rol tanımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="94408-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="94408-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94408-129">CommonParameters</span></span>
<span data-ttu-id="94408-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94408-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94408-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94408-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94408-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94408-132">INPUTS</span></span>

### <span data-ttu-id="94408-133">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="94408-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="94408-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94408-134">OUTPUTS</span></span>

### <span data-ttu-id="94408-135">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="94408-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="94408-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94408-136">NOTES</span></span>
<span data-ttu-id="94408-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="94408-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="94408-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94408-138">RELATED LINKS</span></span>

[<span data-ttu-id="94408-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="94408-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="94408-140">Get-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="94408-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="94408-141">Yeni-Azrol tanımı</span><span class="sxs-lookup"><span data-stu-id="94408-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="94408-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="94408-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

