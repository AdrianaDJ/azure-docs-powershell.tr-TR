---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938113"
---
# <span data-ttu-id="28788-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="28788-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="28788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28788-102">SYNOPSIS</span></span>
<span data-ttu-id="28788-103">Yönetim grubu dağıtımı için dağıtım işlemi alma</span><span class="sxs-lookup"><span data-stu-id="28788-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="28788-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28788-104">SYNTAX</span></span>

### <span data-ttu-id="28788-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28788-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28788-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="28788-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28788-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="28788-107">DESCRIPTION</span></span>
<span data-ttu-id="28788-108">**Get-AzManagementGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için yönetim grubu dağıtımının bir parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="28788-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="28788-109">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="28788-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="28788-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28788-110">EXAMPLES</span></span>

### <span data-ttu-id="28788-111">Örnek 1: dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="28788-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="28788-112">"MyMG" yönetim grubunda "Deploy01" adlı dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="28788-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="28788-113">Örnek 2: dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="28788-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="28788-114">Bu komut, "myMG" yönetim grubundaki "Deploy01" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="28788-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="28788-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28788-115">PARAMETERS</span></span>

### <span data-ttu-id="28788-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="28788-116">-ApiVersion</span></span>
<span data-ttu-id="28788-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="28788-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="28788-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="28788-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="28788-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28788-119">-DefaultProfile</span></span>
<span data-ttu-id="28788-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28788-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28788-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="28788-121">-DeploymentName</span></span>
<span data-ttu-id="28788-122">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="28788-122">The deployment name.</span></span>

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

### <span data-ttu-id="28788-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="28788-123">-DeploymentObject</span></span>
<span data-ttu-id="28788-124">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="28788-124">The deployment object.</span></span>

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

### <span data-ttu-id="28788-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="28788-125">-ManagementGroupId</span></span>
<span data-ttu-id="28788-126">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="28788-126">The management group id.</span></span>

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

### <span data-ttu-id="28788-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="28788-127">-OperationId</span></span>
<span data-ttu-id="28788-128">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="28788-128">The deployment operation Id.</span></span>

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

### <span data-ttu-id="28788-129">-Pre-</span><span class="sxs-lookup"><span data-stu-id="28788-129">-Pre</span></span>
<span data-ttu-id="28788-130">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28788-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="28788-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28788-131">CommonParameters</span></span>
<span data-ttu-id="28788-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28788-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28788-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="28788-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28788-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28788-134">INPUTS</span></span>

### <span data-ttu-id="28788-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="28788-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="28788-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28788-136">OUTPUTS</span></span>

### <span data-ttu-id="28788-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="28788-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="28788-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28788-138">NOTES</span></span>

## <span data-ttu-id="28788-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28788-139">RELATED LINKS</span></span>
