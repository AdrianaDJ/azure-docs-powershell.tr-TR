---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590663"
---
# <span data-ttu-id="92f39-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="92f39-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="92f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f39-102">SYNOPSIS</span></span>
<span data-ttu-id="92f39-103">Azure RBAC 'de özel bir rolü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="92f39-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="92f39-104">Değiştirilmiş rol tanımını JSON dosyası veya PSRoleDefinition olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="92f39-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="92f39-105">İlk olarak, değiştirmek istediğiniz özel rolü almak için Get-AzureRmRoleDefinition komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="92f39-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="92f39-106">Ardından, değiştirmek istediğiniz özellikleri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="92f39-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="92f39-107">Son olarak bu komutu kullanarak rol tanımını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="92f39-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f39-108">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92f39-108">SYNTAX</span></span>

### <span data-ttu-id="92f39-109">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="92f39-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f39-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f39-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92f39-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="92f39-111">DESCRIPTION</span></span>
<span data-ttu-id="92f39-112">Set-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde var olan bir özel rolü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="92f39-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="92f39-113">Güncelleştirilmiş rol tanımını, bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="92f39-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="92f39-114">Güncelleştirilmiş özel rolün rol tanımı, güncelleştirilmese bile, rolün kimliğini ve tüm diğer gerekli özelliklerini içermelidir: DisplayName, Description, Actions, Astifblescopes.</span><span class="sxs-lookup"><span data-stu-id="92f39-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="92f39-115">NotActions isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="92f39-115">NotActions is optional.</span></span>

<span data-ttu-id="92f39-116">Aşağıda, Set-AzureRmRoleDefinition için güncelleştirilmiş bir rol tanımı JSON 'i verilmiştir</span><span class="sxs-lookup"><span data-stu-id="92f39-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="92f39-117">{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "güncelleştirilmiş rol", "Açıklama": "tüm kaynakları izleyebilir ve sanal makineleri başlatıp yeniden başlatabilirsiniz", "eylemler": \[ "\*/Read", "Microsoft. Classıntericcompute/virtualmachines/restart/ACTION", "Microsoft. Classıntericcompute/sanall/Başlat/eylem" \] "astifblescopes": \[ "/Subscriptions/4004a6fd-vseç58e-48dc-aeb2-4a4aec58606f" \] }</span><span class="sxs-lookup"><span data-stu-id="92f39-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "\*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \["/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f"\] }</span></span>

## <span data-ttu-id="92f39-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92f39-118">EXAMPLES</span></span>

### <span data-ttu-id="92f39-119">PSRoleDefinitionObject--------------------------kullanarak--------------------------güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="92f39-119">--------------------------  Update using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="92f39-120">JSON dosyası kullanarak oluşturma----------------------------------------------------</span><span class="sxs-lookup"><span data-stu-id="92f39-120">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="92f39-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92f39-121">PARAMETERS</span></span>

### <span data-ttu-id="92f39-122">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="92f39-122">-InputFile</span></span>
<span data-ttu-id="92f39-123">Güncelleştirilecek tek bir JSON rol tanımı içeren dosya adı.</span><span class="sxs-lookup"><span data-stu-id="92f39-123">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="92f39-124">Yalnızca JSON 'de güncelleştirilecek özellikleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="92f39-124">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="92f39-125">ID özelliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="92f39-125">Id property is Required.</span></span>

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

### <span data-ttu-id="92f39-126">-Role</span><span class="sxs-lookup"><span data-stu-id="92f39-126">-Role</span></span>
<span data-ttu-id="92f39-127">Güncelleştirilecek rol tanımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="92f39-127">Role definition object to be updated</span></span>

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

### <span data-ttu-id="92f39-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f39-128">-DefaultProfile</span></span>
<span data-ttu-id="92f39-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92f39-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f39-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f39-130">CommonParameters</span></span>
<span data-ttu-id="92f39-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92f39-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f39-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f39-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f39-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92f39-133">INPUTS</span></span>

### <span data-ttu-id="92f39-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="92f39-134">PSRoleDefinition</span></span>
<span data-ttu-id="92f39-135">Parametre ' rol ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="92f39-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="92f39-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92f39-136">OUTPUTS</span></span>

### <span data-ttu-id="92f39-137">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="92f39-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="92f39-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92f39-138">NOTES</span></span>
<span data-ttu-id="92f39-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="92f39-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="92f39-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92f39-140">RELATED LINKS</span></span>

[<span data-ttu-id="92f39-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="92f39-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="92f39-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="92f39-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="92f39-143">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="92f39-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="92f39-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="92f39-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

