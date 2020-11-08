---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274227"
---
# <span data-ttu-id="955c7-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="955c7-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="955c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="955c7-102">SYNOPSIS</span></span>
<span data-ttu-id="955c7-103">Yönetim grubunda dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="955c7-103">Get deployment at a management group</span></span>

## <span data-ttu-id="955c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="955c7-104">SYNTAX</span></span>

### <span data-ttu-id="955c7-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="955c7-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="955c7-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="955c7-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="955c7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="955c7-107">DESCRIPTION</span></span>
<span data-ttu-id="955c7-108">**Get-AzManagementGroupDeployment** cmdlet 'i bir yönetim grubundaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="955c7-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="955c7-109">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="955c7-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="955c7-110">**Get-AzManagementGroupDeployment** , varsayılan olarak yönetim grubundaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="955c7-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="955c7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="955c7-111">EXAMPLES</span></span>

### <span data-ttu-id="955c7-112">Örnek 1: yönetim grubundaki tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="955c7-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="955c7-113">Bu komut, "myMG" yönetim grubundaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="955c7-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="955c7-114">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="955c7-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="955c7-115">Bu komut, "myMG" yönetim grubunda "Deploy01" dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="955c7-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="955c7-116">**Yeni-AzManagementGroupDeployment** cmdlet 'lerini kullanarak oluşturduğunuz dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="955c7-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="955c7-117">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="955c7-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="955c7-118">Örnek 3: KIMLIĞE göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="955c7-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="955c7-119">Bu komut, "myMG" yönetim grubunda "Deploy01" dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="955c7-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="955c7-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="955c7-120">PARAMETERS</span></span>

### <span data-ttu-id="955c7-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="955c7-121">-ApiVersion</span></span>
<span data-ttu-id="955c7-122">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="955c7-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="955c7-123">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="955c7-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955c7-124">-DefaultProfile</span></span>
<span data-ttu-id="955c7-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="955c7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c7-126">-ID</span><span class="sxs-lookup"><span data-stu-id="955c7-126">-Id</span></span>
<span data-ttu-id="955c7-127">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="955c7-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="955c7-128">Örnek:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="955c7-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c7-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="955c7-129">-ManagementGroupId</span></span>
<span data-ttu-id="955c7-130">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="955c7-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c7-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="955c7-131">-Name</span></span>
<span data-ttu-id="955c7-132">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="955c7-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c7-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="955c7-133">-Pre</span></span>
<span data-ttu-id="955c7-134">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="955c7-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955c7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955c7-135">CommonParameters</span></span>
<span data-ttu-id="955c7-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="955c7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955c7-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="955c7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955c7-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="955c7-138">INPUTS</span></span>

### <span data-ttu-id="955c7-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="955c7-139">None</span></span>

## <span data-ttu-id="955c7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="955c7-140">OUTPUTS</span></span>

### <span data-ttu-id="955c7-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="955c7-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="955c7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="955c7-142">NOTES</span></span>

## <span data-ttu-id="955c7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="955c7-143">RELATED LINKS</span></span>
