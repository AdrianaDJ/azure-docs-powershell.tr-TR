---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939049"
---
# <span data-ttu-id="1bb16-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1bb16-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="1bb16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bb16-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb16-103">Dağıtımı al</span><span class="sxs-lookup"><span data-stu-id="1bb16-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bb16-104">SYNTAX</span></span>

### <span data-ttu-id="1bb16-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1bb16-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bb16-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1bb16-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bb16-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bb16-107">DESCRIPTION</span></span>
<span data-ttu-id="1bb16-108">**Get-AzureRmDeployment** cmdlet 'i geçerli abonelik kapsamındaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="1bb16-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="1bb16-109">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1bb16-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="1bb16-110">**Get-AzureRmDeployment** , varsayılan olarak geçerli abonelik kapsamındaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="1bb16-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="1bb16-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bb16-111">EXAMPLES</span></span>

### <span data-ttu-id="1bb16-112">Örnek 1: abonelik kapsamındaki tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="1bb16-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="1bb16-113">Bu komut, geçerli abonelik kapsamındaki tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="1bb16-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="1bb16-114">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="1bb16-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="1bb16-115">Bu komut, geçerli abonelik kapsamında DeployRoles01 dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="1bb16-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="1bb16-116">**Yeni-AzureRmDeployment** cmdlet 'lerini kullanarak oluşturduğunuz dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bb16-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="1bb16-117">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="1bb16-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="1bb16-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bb16-118">PARAMETERS</span></span>

### <span data-ttu-id="1bb16-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="1bb16-119">-ApiVersion</span></span>
<span data-ttu-id="1bb16-120">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="1bb16-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1bb16-121">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1bb16-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1bb16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb16-122">-DefaultProfile</span></span>
<span data-ttu-id="1bb16-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1bb16-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb16-124">-ID</span><span class="sxs-lookup"><span data-stu-id="1bb16-124">-Id</span></span>
<span data-ttu-id="1bb16-125">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1bb16-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="1bb16-126">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="1bb16-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb16-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="1bb16-127">-Name</span></span>
<span data-ttu-id="1bb16-128">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="1bb16-128">The name of deployment.</span></span>

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

### <span data-ttu-id="1bb16-129">-Pre-</span><span class="sxs-lookup"><span data-stu-id="1bb16-129">-Pre</span></span>
<span data-ttu-id="1bb16-130">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bb16-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1bb16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb16-131">CommonParameters</span></span>
<span data-ttu-id="1bb16-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bb16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb16-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb16-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb16-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bb16-134">INPUTS</span></span>

### <span data-ttu-id="1bb16-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb16-135">System.String</span></span>

## <span data-ttu-id="1bb16-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bb16-136">OUTPUTS</span></span>

### <span data-ttu-id="1bb16-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="1bb16-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1bb16-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bb16-138">NOTES</span></span>

## <span data-ttu-id="1bb16-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bb16-139">RELATED LINKS</span></span>
