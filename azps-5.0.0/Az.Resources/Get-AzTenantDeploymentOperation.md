---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322891"
---
# <span data-ttu-id="ce181-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ce181-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="ce181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce181-102">SYNOPSIS</span></span>
<span data-ttu-id="ce181-103">Kiracı kapsamındaki dağıtım için dağıtım işlemini alma</span><span class="sxs-lookup"><span data-stu-id="ce181-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="ce181-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce181-104">SYNTAX</span></span>

### <span data-ttu-id="ce181-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce181-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce181-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ce181-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce181-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce181-107">DESCRIPTION</span></span>
<span data-ttu-id="ce181-108">**Get-AzTenantDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için geçerli kiracı kapsamında dağıtımın bir parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="ce181-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="ce181-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce181-109">EXAMPLES</span></span>

### <span data-ttu-id="ce181-110">Örnek 1: dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="ce181-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="ce181-111">Geçerli kiracı kapsamındaki "Deploy01" adlı dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ce181-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="ce181-112">Örnek 2: dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="ce181-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="ce181-113">Bu komut, geçerli kiracı kapsamındaki "Deploy01" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ce181-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="ce181-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce181-114">PARAMETERS</span></span>

### <span data-ttu-id="ce181-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce181-115">-DefaultProfile</span></span>
<span data-ttu-id="ce181-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce181-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce181-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="ce181-117">-DeploymentName</span></span>
<span data-ttu-id="ce181-118">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="ce181-118">The deployment name.</span></span>

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

### <span data-ttu-id="ce181-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ce181-119">-DeploymentObject</span></span>
<span data-ttu-id="ce181-120">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ce181-120">The deployment object.</span></span>

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

### <span data-ttu-id="ce181-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ce181-121">-OperationId</span></span>
<span data-ttu-id="ce181-122">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="ce181-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="ce181-123">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ce181-123">-Pre</span></span>
<span data-ttu-id="ce181-124">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce181-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ce181-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce181-125">CommonParameters</span></span>
<span data-ttu-id="ce181-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce181-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce181-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ce181-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce181-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce181-128">INPUTS</span></span>

### <span data-ttu-id="ce181-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="ce181-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ce181-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce181-130">OUTPUTS</span></span>

### <span data-ttu-id="ce181-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ce181-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="ce181-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce181-132">NOTES</span></span>

## <span data-ttu-id="ce181-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce181-133">RELATED LINKS</span></span>
