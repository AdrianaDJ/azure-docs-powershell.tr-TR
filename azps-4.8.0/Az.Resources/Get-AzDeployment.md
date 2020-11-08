---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 5ea6e36adeb1c0b220b87d516e9c236907bc2c63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266463"
---
# <span data-ttu-id="c7f1a-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c7f1a-101">Get-AzDeployment</span></span>

## <span data-ttu-id="c7f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f1a-103">Dağıtımı al</span><span class="sxs-lookup"><span data-stu-id="c7f1a-103">Get deployment</span></span>

## <span data-ttu-id="c7f1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7f1a-104">SYNTAX</span></span>

### <span data-ttu-id="c7f1a-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7f1a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7f1a-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c7f1a-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7f1a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7f1a-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f1a-108">**Get-AzDeployment** cmdlet 'i geçerli abonelik kapsamındaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="c7f1a-109">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="c7f1a-110">**Get-AzDeployment** , varsayılan olarak geçerli abonelik kapsamındaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="c7f1a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7f1a-111">EXAMPLES</span></span>

### <span data-ttu-id="c7f1a-112">Örnek 1: abonelik kapsamındaki tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="c7f1a-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="c7f1a-113">Bu komut, geçerli abonelik kapsamındaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="c7f1a-114">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="c7f1a-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="c7f1a-115">Bu komut, geçerli abonelik kapsamında DeployRoles01 dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="c7f1a-116">**Yeni-Azdağıtım** cmdlet 'lerini kullanarak oluşturduğunuz bir dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="c7f1a-117">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="c7f1a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7f1a-118">PARAMETERS</span></span>

### <span data-ttu-id="c7f1a-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c7f1a-119">-ApiVersion</span></span>
<span data-ttu-id="c7f1a-120">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c7f1a-121">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-121">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f1a-122">-DefaultProfile</span></span>
<span data-ttu-id="c7f1a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7f1a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c7f1a-124">-Id</span></span>
<span data-ttu-id="c7f1a-125">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c7f1a-126">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c7f1a-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f1a-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7f1a-127">-Name</span></span>
<span data-ttu-id="c7f1a-128">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-128">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f1a-129">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c7f1a-129">-Pre</span></span>
<span data-ttu-id="c7f1a-130">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f1a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f1a-131">CommonParameters</span></span>
<span data-ttu-id="c7f1a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f1a-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c7f1a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f1a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7f1a-134">INPUTS</span></span>

### <span data-ttu-id="c7f1a-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c7f1a-135">None</span></span>

## <span data-ttu-id="c7f1a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7f1a-136">OUTPUTS</span></span>

### <span data-ttu-id="c7f1a-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="c7f1a-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c7f1a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7f1a-138">NOTES</span></span>

## <span data-ttu-id="c7f1a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7f1a-139">RELATED LINKS</span></span>
