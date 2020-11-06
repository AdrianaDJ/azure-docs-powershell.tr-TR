---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592568"
---
# <span data-ttu-id="f3b2d-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f3b2d-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="f3b2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b2d-103">Azure RBAC 'de özel bir rol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f3b2d-104">Giriş olarak bir JSON rol tanımı dosyası veya PSRoleDefinition nesnesi sağlayın.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="f3b2d-105">İlk olarak, temel rol tanımı nesnesi oluşturmak için Get-AzureRmRoleDefinition komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="f3b2d-106">Ardından özelliklerini gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="f3b2d-107">Son olarak, rol tanımını kullanarak özel bir rol oluşturmak için bu komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3b2d-108">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3b2d-108">SYNTAX</span></span>

### <span data-ttu-id="f3b2d-109">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="f3b2d-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3b2d-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b2d-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3b2d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3b2d-111">DESCRIPTION</span></span>
<span data-ttu-id="f3b2d-112">New-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f3b2d-113">Bir rol tanımını bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="f3b2d-114">Giriş rol tanımında aşağıdaki özellikler bulunmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f3b2d-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="f3b2d-115">DisplayName: özel rolün adı</span><span class="sxs-lookup"><span data-stu-id="f3b2d-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="f3b2d-116">Açıklama: rolün verdiği erişimi özetleyen rolün kısa bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="f3b2d-117">Eylemler: özel rolün erişim verdiği işlemler kümesi.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="f3b2d-118">Azure RBAC kullanılarak güvenliği sağlansağlanan Azure Kaynak sağlayıcılarının işlemini edinmek için Get-AzureRmProviderOperations kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-118">Use Get-AzureRmProviderOperations to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="f3b2d-119">Aşağıda bazı geçerli işlem dizeleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="f3b2d-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="f3b2d-120">"\*/Read" tüm Azure Resource sağlayıcılarının okuma işlemlerine erişim verir.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="f3b2d-121">"Microsoft. Network/\*/Read" Azure 'un Microsoft. Network Resource Provider 'daki tüm kaynak türlerinin okuma işlemlerine erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="f3b2d-122">"Microsoft. COMPUTE/virtualMachines/\*" sanal makinelerin tüm işlemlerine ve alt kaynak türlerine erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="f3b2d-123">Astabeblescopes: özel rolün atama için kullanılabileceği kapsam kümesi (Azure abonelikleri veya kaynak grupları).</span><span class="sxs-lookup"><span data-stu-id="f3b2d-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="f3b2d-124">Astifblescopes 'ı kullanarak, özel rolü yalnızca gerekli olan aboneliklere veya kaynak gruplarında kullanılabilir hale getirebilirsiniz ve aboneliğin veya kaynak gruplarının geri kalanı için Kullanıcı deneyimini ikincil haline getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="f3b2d-125">Aşağıdakiler geçerli atanabilir kapsamlardır:</span><span class="sxs-lookup"><span data-stu-id="f3b2d-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="f3b2d-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rolün iki abonelikteki ödev için kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="f3b2d-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": rolün tek bir abonelikte ödev için kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="f3b2d-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rolün yalnızca ağ kaynak grubundaki ödev için kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="f3b2d-129">Giriş rol tanımı aşağıdaki özellikleri içerebilir:</span><span class="sxs-lookup"><span data-stu-id="f3b2d-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="f3b2d-130">NotActions: özel rolün etkili eylemlerini belirlemek için eylemlerin dışında tutulması gereken işlemler kümesi.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="f3b2d-131">Özel bir rolde erişim vermek istemediğiniz belirli bir işlem varsa, bu belirli işlemler yerine bu belirli işlemler dışında tüm işlemleri belirtmek yerine NotActions 'ı kullanmak uygun olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="f3b2d-132">Not: kullanıcıya, NotActions 'da bir işlemi belirten bir rol atanmışsa ve başka bir rolün aynı işleme erişim izni verdiğini düşünüyorsanız, Kullanıcı bu işlemi gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-132">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="f3b2d-133">NotActions, bir Reddedilenler kuralı değil; belirli işlemler dışlanmak gerektiğinde izin verilen işlemler kümesi oluşturmanın kullanışlı bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-133">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="f3b2d-134">Aşağıda, giriş {"ad" olarak sağlansağlanan örnek bir JSON rol tanımı verilmiştir: "contoso On-Call", "Açıklama": "işlem, ağ ve depolamayı izleyebilir ve sanal makineleri", "eylemler": \[ "Microsoft. COMPUTE/ */Read", "Microsoft. COMPUTE/sanalmakine/Başlat/eylem", "Microsoft. COMPUTE/virtualmachines/restart/ACTION", "Microsoft. COMPUTE/Virtualmachines/downloadRemoteDesktopConnectionFile/ACTION", "Microsoft. Network/* /Read", "Microsoft. Storage/ */Read", "Microsoft. Authorization/* /Read", "Microsoft. resources/aboneliklerin/ResourceGroups/Read", "Microsoft/ *", "Microsoft. support/* " \] , "astifblescopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/Subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy" \] }</span><span class="sxs-lookup"><span data-stu-id="f3b2d-134">Following is a sample json role definition that can be provided as input { "Name": "Contoso On-call", "Description": "Can monitor compute, network and storage, and restart virtual machines", "Actions": \[ "Microsoft.Compute/ */read", "Microsoft.Compute/virtualMachines/start/action", "Microsoft.Compute/virtualMachines/restart/action", "Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action", "Microsoft.Network/* /read", "Microsoft.Storage/ */read", "Microsoft.Authorization/* /read", "Microsoft.Resources/subscriptions/resourceGroups/read", "Microsoft.Resources/subscriptions/resourceGroups/resources/read", "Microsoft.Insights/alertRules/ *", "Microsoft.Support/* " \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx","/subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"\] }</span></span>

## <span data-ttu-id="f3b2d-135">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3b2d-135">EXAMPLES</span></span>

### <span data-ttu-id="f3b2d-136">PSRoleDefinitionObject--------------------------kullanarak oluşturma--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3b2d-136">--------------------------  Create using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="f3b2d-137">JSON dosyası kullanarak oluşturma----------------------------------------------------</span><span class="sxs-lookup"><span data-stu-id="f3b2d-137">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="f3b2d-138">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3b2d-138">PARAMETERS</span></span>

### <span data-ttu-id="f3b2d-139">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="f3b2d-139">-InputFile</span></span>
<span data-ttu-id="f3b2d-140">Tek bir JSON rol tanımını içeren dosya adı.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-140">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="f3b2d-141">-Role</span><span class="sxs-lookup"><span data-stu-id="f3b2d-141">-Role</span></span>
<span data-ttu-id="f3b2d-142">Rol tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-142">Role definition object.</span></span>

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

### <span data-ttu-id="f3b2d-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b2d-143">-DefaultProfile</span></span>
<span data-ttu-id="f3b2d-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b2d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b2d-145">CommonParameters</span></span>
<span data-ttu-id="f3b2d-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3b2d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b2d-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b2d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b2d-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3b2d-148">INPUTS</span></span>

## <span data-ttu-id="f3b2d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3b2d-149">OUTPUTS</span></span>

### <span data-ttu-id="f3b2d-150">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f3b2d-150">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f3b2d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3b2d-151">NOTES</span></span>
<span data-ttu-id="f3b2d-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="f3b2d-152">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f3b2d-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3b2d-153">RELATED LINKS</span></span>

[<span data-ttu-id="f3b2d-154">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="f3b2d-154">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="f3b2d-155">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f3b2d-155">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="f3b2d-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f3b2d-156">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="f3b2d-157">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f3b2d-157">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

