---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109352"
---
# <span data-ttu-id="803d3-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="803d3-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="803d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="803d3-102">SYNOPSIS</span></span>
<span data-ttu-id="803d3-103">Kiracı kapsamında dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="803d3-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="803d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="803d3-104">SYNTAX</span></span>

### <span data-ttu-id="803d3-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="803d3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="803d3-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="803d3-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="803d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="803d3-107">DESCRIPTION</span></span>
<span data-ttu-id="803d3-108">**Get-AzTenantDeployment** cmdlet 'i kiracı kapsamındaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="803d3-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="803d3-109">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="803d3-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="803d3-110">**Get-AzTenantDeployment** , varsayılan olarak kiracı kapsamındaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="803d3-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="803d3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="803d3-111">EXAMPLES</span></span>

### <span data-ttu-id="803d3-112">Örnek 1: kiracı kapsamındaki tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="803d3-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="803d3-113">Bu komut, geçerli kiracı kapsamındaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="803d3-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="803d3-114">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="803d3-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="803d3-115">Bu komut, geçerli kiracı kapsamındaki "Deploy01" dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="803d3-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="803d3-116">**Yeni-AzTenantDeployment** cmdlet 'lerini kullanarak oluşturduğunuz dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="803d3-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="803d3-117">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="803d3-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="803d3-118">Örnek 3: KIMLIĞE göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="803d3-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="803d3-119">Bu komut, kiracı kapsamında "Deploy01" dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="803d3-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="803d3-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="803d3-120">PARAMETERS</span></span>

### <span data-ttu-id="803d3-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="803d3-121">-ApiVersion</span></span>
<span data-ttu-id="803d3-122">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="803d3-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="803d3-123">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="803d3-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="803d3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803d3-124">-DefaultProfile</span></span>
<span data-ttu-id="803d3-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="803d3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="803d3-126">-ID</span><span class="sxs-lookup"><span data-stu-id="803d3-126">-Id</span></span>
<span data-ttu-id="803d3-127">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="803d3-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="803d3-128">Örnek:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="803d3-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="803d3-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="803d3-129">-Name</span></span>
<span data-ttu-id="803d3-130">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="803d3-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="803d3-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="803d3-131">-Pre</span></span>
<span data-ttu-id="803d3-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="803d3-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="803d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803d3-133">CommonParameters</span></span>
<span data-ttu-id="803d3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="803d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803d3-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="803d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803d3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="803d3-136">INPUTS</span></span>

### <span data-ttu-id="803d3-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="803d3-137">None</span></span>

## <span data-ttu-id="803d3-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="803d3-138">OUTPUTS</span></span>

### <span data-ttu-id="803d3-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="803d3-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="803d3-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="803d3-140">NOTES</span></span>

## <span data-ttu-id="803d3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="803d3-141">RELATED LINKS</span></span>
