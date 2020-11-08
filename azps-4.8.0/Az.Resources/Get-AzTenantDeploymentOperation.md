---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268823"
---
# <span data-ttu-id="aebd6-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="aebd6-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="aebd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aebd6-102">SYNOPSIS</span></span>
<span data-ttu-id="aebd6-103">Kiracı kapsamındaki dağıtım için dağıtım işlemini alma</span><span class="sxs-lookup"><span data-stu-id="aebd6-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="aebd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aebd6-104">SYNTAX</span></span>

### <span data-ttu-id="aebd6-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aebd6-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aebd6-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="aebd6-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aebd6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aebd6-107">DESCRIPTION</span></span>
<span data-ttu-id="aebd6-108">**Get-AzTenantDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için geçerli kiracı kapsamında dağıtımın bir parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="aebd6-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="aebd6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aebd6-109">EXAMPLES</span></span>

### <span data-ttu-id="aebd6-110">Örnek 1: dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="aebd6-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="aebd6-111">Geçerli kiracı kapsamındaki "Deploy01" adlı dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="aebd6-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="aebd6-112">Örnek 2: dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="aebd6-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="aebd6-113">Bu komut, geçerli kiracı kapsamındaki "Deploy01" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="aebd6-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="aebd6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aebd6-114">PARAMETERS</span></span>

### <span data-ttu-id="aebd6-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="aebd6-115">-ApiVersion</span></span>
<span data-ttu-id="aebd6-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="aebd6-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="aebd6-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aebd6-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="aebd6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebd6-118">-DefaultProfile</span></span>
<span data-ttu-id="aebd6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aebd6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aebd6-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="aebd6-120">-DeploymentName</span></span>
<span data-ttu-id="aebd6-121">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="aebd6-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebd6-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="aebd6-122">-DeploymentObject</span></span>
<span data-ttu-id="aebd6-123">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aebd6-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aebd6-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="aebd6-124">-OperationId</span></span>
<span data-ttu-id="aebd6-125">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="aebd6-125">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebd6-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="aebd6-126">-Pre</span></span>
<span data-ttu-id="aebd6-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aebd6-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="aebd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebd6-128">CommonParameters</span></span>
<span data-ttu-id="aebd6-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aebd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebd6-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aebd6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebd6-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aebd6-131">INPUTS</span></span>

### <span data-ttu-id="aebd6-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="aebd6-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="aebd6-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aebd6-133">OUTPUTS</span></span>

### <span data-ttu-id="aebd6-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="aebd6-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="aebd6-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aebd6-135">NOTES</span></span>

## <span data-ttu-id="aebd6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aebd6-136">RELATED LINKS</span></span>
