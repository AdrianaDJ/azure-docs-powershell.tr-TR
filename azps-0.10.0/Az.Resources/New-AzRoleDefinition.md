---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 40747a82cab67a61e6a65e9eba4f3ba6ebc66f96
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936382"
---
# <span data-ttu-id="54ad4-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54ad4-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="54ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="54ad4-103">Azure RBAC 'de özel bir rol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54ad4-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="54ad4-104">Giriş olarak bir JSON rol tanımı dosyası veya PSRoleDefinition nesnesi sağlayın.</span><span class="sxs-lookup"><span data-stu-id="54ad4-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="54ad4-105">İlk olarak, temel rol tanımı nesnesi oluşturmak için Get-AzRoleDefinition komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="54ad4-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="54ad4-106">Ardından özelliklerini gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="54ad4-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="54ad4-107">Son olarak, rol tanımını kullanarak özel bir rol oluşturmak için bu komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="54ad4-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="54ad4-108">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54ad4-108">SYNTAX</span></span>

### <span data-ttu-id="54ad4-109">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="54ad4-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54ad4-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="54ad4-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54ad4-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="54ad4-111">DESCRIPTION</span></span>
<span data-ttu-id="54ad4-112">New-AzRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54ad4-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="54ad4-113">Bir rol tanımını bir JSON dosyası veya PSRoleDefinition nesnesi olarak komuta giriş olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="54ad4-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="54ad4-114">Giriş rol tanımında aşağıdaki özellikler bulunmalıdır:</span><span class="sxs-lookup"><span data-stu-id="54ad4-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="54ad4-115">DisplayName: özel rolün adı</span><span class="sxs-lookup"><span data-stu-id="54ad4-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="54ad4-116">Açıklama: rolün verdiği erişimi özetleyen rolün kısa bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="54ad4-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="54ad4-117">Eylemler: özel rolün erişim verdiği işlemler kümesi.</span><span class="sxs-lookup"><span data-stu-id="54ad4-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="54ad4-118">Azure RBAC kullanılarak güvenliği sağlansağlanan Azure Kaynak sağlayıcılarının işlemini edinmek için Get-AzProviderOperation kullanın.</span><span class="sxs-lookup"><span data-stu-id="54ad4-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="54ad4-119">Aşağıda bazı geçerli işlem dizeleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="54ad4-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="54ad4-120">"\*/Read" tüm Azure Resource sağlayıcılarının okuma işlemlerine erişim verir.</span><span class="sxs-lookup"><span data-stu-id="54ad4-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="54ad4-121">"Microsoft. Network/\*/Read" Azure 'un Microsoft. Network Resource Provider 'daki tüm kaynak türlerinin okuma işlemlerine erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="54ad4-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="54ad4-122">"Microsoft. COMPUTE/virtualMachines/\*" sanal makinelerin tüm işlemlerine ve alt kaynak türlerine erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="54ad4-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="54ad4-123">Astabeblescopes: özel rolün atama için kullanılabileceği kapsam kümesi (Azure abonelikleri veya kaynak grupları).</span><span class="sxs-lookup"><span data-stu-id="54ad4-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="54ad4-124">Astifblescopes 'ı kullanarak, özel rolü yalnızca gerekli olan aboneliklere veya kaynak gruplarında kullanılabilir hale getirebilirsiniz ve aboneliğin veya kaynak gruplarının geri kalanı için Kullanıcı deneyimini ikincil haline getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="54ad4-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="54ad4-125">Aşağıdakiler geçerli atanabilir kapsamlardır:</span><span class="sxs-lookup"><span data-stu-id="54ad4-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="54ad4-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rolün iki abonelikteki ödev için kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="54ad4-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="54ad4-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": rolün tek bir abonelikte ödev için kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="54ad4-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="54ad4-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rolün yalnızca ağ kaynak grubundaki ödev için kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="54ad4-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="54ad4-129">Giriş rol tanımı aşağıdaki özellikleri içerebilir:</span><span class="sxs-lookup"><span data-stu-id="54ad4-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="54ad4-130">NotActions: özel rolün etkili eylemlerini belirlemek için eylemlerin dışında tutulması gereken işlemler kümesi.</span><span class="sxs-lookup"><span data-stu-id="54ad4-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="54ad4-131">Özel bir rolde erişim vermek istemediğiniz belirli bir işlem varsa, bu belirli işlemler yerine bu belirli işlemler dışında tüm işlemleri belirtmek yerine NotActions 'ı kullanmak uygun olacaktır.</span><span class="sxs-lookup"><span data-stu-id="54ad4-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="54ad4-132">DataActions: özel rolün erişim verdiği veri işlemleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="54ad4-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="54ad4-133">Notvereylemler: özel rolün etkin veri eylemlerini belirlemek için DataActions 'tan dışlanması gereken işlemler kümesi.</span><span class="sxs-lookup"><span data-stu-id="54ad4-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective dataactions for the custom role.</span></span>
<span data-ttu-id="54ad4-134">Özel bir rolde erişim vermek istemediğiniz belirli bir veri işlemi varsa, eylemlerdeki belirli işlemler dışında tüm işlemleri yerine çıkarmak için NotDataActions 'ı kullanmak kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="54ad4-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="54ad4-135">Not: kullanıcıya, NotActions 'da bir işlemi belirten bir rol atanmışsa ve başka bir rolün aynı işleme erişim izni verdiğini düşünüyorsanız, Kullanıcı bu işlemi gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="54ad4-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="54ad4-136">NotActions, bir Reddedilenler kuralı değil; belirli işlemler dışlanmak gerektiğinde izin verilen işlemler kümesi oluşturmanın kullanışlı bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="54ad4-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="54ad4-137">Aşağıda, giriş {"ad": "güncelleştirilen rol", "Açıklama": "tüm kaynakları izleyebilir,", "eylemler": \[ " */Read", "Microsoft. Classıntericcompute/virtualmachines/restart/Action", "Microsoft. classıntericcompute/virtualmachines/restart/Action" \] , "NotActions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Read" \] , "Notdataactions": \[ "Microsoft. Storage/storageaccounts/blobservices/kapsayıcılar/blob/Write" \] \[ \]</span><span class="sxs-lookup"><span data-stu-id="54ad4-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="54ad4-138">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54ad4-138">EXAMPLES</span></span>

### <span data-ttu-id="54ad4-139">PSRoleDefinitionObject kullanarak oluşturma</span><span class="sxs-lookup"><span data-stu-id="54ad4-139">Create using PSRoleDefinitionObject</span></span>
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

### <span data-ttu-id="54ad4-140">JSON dosyası kullanarak oluştur</span><span class="sxs-lookup"><span data-stu-id="54ad4-140">Create using JSON file</span></span>
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="54ad4-141">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54ad4-141">PARAMETERS</span></span>

### <span data-ttu-id="54ad4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ad4-142">-DefaultProfile</span></span>
<span data-ttu-id="54ad4-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="54ad4-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ad4-144">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="54ad4-144">-InputFile</span></span>
<span data-ttu-id="54ad4-145">Tek bir JSON rol tanımını içeren dosya adı.</span><span class="sxs-lookup"><span data-stu-id="54ad4-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="54ad4-146">-Role</span><span class="sxs-lookup"><span data-stu-id="54ad4-146">-Role</span></span>
<span data-ttu-id="54ad4-147">Rol tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="54ad4-147">Role definition object.</span></span>

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

### <span data-ttu-id="54ad4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ad4-148">CommonParameters</span></span>
<span data-ttu-id="54ad4-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54ad4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ad4-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ad4-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ad4-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54ad4-151">INPUTS</span></span>

### <span data-ttu-id="54ad4-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="54ad4-152">None</span></span>

## <span data-ttu-id="54ad4-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54ad4-153">OUTPUTS</span></span>

### <span data-ttu-id="54ad4-154">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54ad4-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="54ad4-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54ad4-155">NOTES</span></span>
<span data-ttu-id="54ad4-156">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="54ad4-156">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="54ad4-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54ad4-157">RELATED LINKS</span></span>

[<span data-ttu-id="54ad4-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="54ad4-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="54ad4-159">Get-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="54ad4-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="54ad4-160">Set-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="54ad4-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="54ad4-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54ad4-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

