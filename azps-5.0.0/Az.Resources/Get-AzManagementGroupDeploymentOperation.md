---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323002"
---
# <span data-ttu-id="9c567-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9c567-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="9c567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c567-102">SYNOPSIS</span></span>
<span data-ttu-id="9c567-103">Yönetim grubu dağıtımı için dağıtım işlemi alma</span><span class="sxs-lookup"><span data-stu-id="9c567-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="9c567-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c567-104">SYNTAX</span></span>

### <span data-ttu-id="9c567-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c567-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c567-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9c567-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c567-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c567-107">DESCRIPTION</span></span>
<span data-ttu-id="9c567-108">**Get-AzManagementGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için yönetim grubu dağıtımının bir parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="9c567-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="9c567-109">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="9c567-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="9c567-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c567-110">EXAMPLES</span></span>

### <span data-ttu-id="9c567-111">Örnek 1: dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="9c567-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="9c567-112">"MyMG" yönetim grubunda "Deploy01" adlı dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9c567-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="9c567-113">Örnek 2: dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="9c567-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="9c567-114">Bu komut, "myMG" yönetim grubundaki "Deploy01" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9c567-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="9c567-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c567-115">PARAMETERS</span></span>

### <span data-ttu-id="9c567-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c567-116">-DefaultProfile</span></span>
<span data-ttu-id="9c567-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c567-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c567-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9c567-118">-DeploymentName</span></span>
<span data-ttu-id="9c567-119">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="9c567-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c567-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9c567-120">-DeploymentObject</span></span>
<span data-ttu-id="9c567-121">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9c567-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c567-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9c567-122">-ManagementGroupId</span></span>
<span data-ttu-id="9c567-123">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="9c567-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c567-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9c567-124">-OperationId</span></span>
<span data-ttu-id="9c567-125">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="9c567-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c567-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9c567-126">-Pre</span></span>
<span data-ttu-id="9c567-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c567-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9c567-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c567-128">CommonParameters</span></span>
<span data-ttu-id="9c567-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c567-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c567-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9c567-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c567-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c567-131">INPUTS</span></span>

### <span data-ttu-id="9c567-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="9c567-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9c567-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c567-133">OUTPUTS</span></span>

### <span data-ttu-id="9c567-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9c567-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="9c567-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c567-135">NOTES</span></span>

## <span data-ttu-id="9c567-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c567-136">RELATED LINKS</span></span>
