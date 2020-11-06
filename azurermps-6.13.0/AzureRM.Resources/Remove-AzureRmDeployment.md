---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmDeployment.md
ms.openlocfilehash: a008ecf8b8c6681941e19b4db63f79c85fab8ba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589370"
---
# <span data-ttu-id="f9800-101">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9800-101">Remove-AzureRmDeployment</span></span>

## <span data-ttu-id="f9800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9800-102">SYNOPSIS</span></span>
<span data-ttu-id="f9800-103">Bir dağıtımı ve ilişkili işlemleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="f9800-103">Removes a deployment and any associated operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9800-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9800-104">SYNTAX</span></span>

### <span data-ttu-id="f9800-105">RemoveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9800-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzureRmDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9800-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f9800-106">RemoveByDeploymentId</span></span>
```
Remove-AzureRmDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9800-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9800-107">RemoveByInputObject</span></span>
```
Remove-AzureRmDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9800-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9800-108">DESCRIPTION</span></span>
<span data-ttu-id="f9800-109">**Remove-AzureRmDeployment** cmdlet 'i abonelik kapsamındaki bir Azure dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9800-109">The **Remove-AzureRmDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="f9800-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9800-110">EXAMPLES</span></span>

### <span data-ttu-id="f9800-111">Örnek 1: verilen bir ada sahip bir dağıtımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f9800-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzureRmDeployment -Name "RolesDeployment"
```

<span data-ttu-id="f9800-112">Bu komut, geçerli abonelik kapsamındaki "RolesDeployment" dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9800-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="f9800-113">Örnek 2: bir dağıtım alın ve kaldırın</span><span class="sxs-lookup"><span data-stu-id="f9800-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Remove-AzureRmDeployment
```

<span data-ttu-id="f9800-114">Bu komut, geçerli abonelik kapsamındaki "RolesDeployment" dağıtımını alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9800-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="f9800-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9800-115">PARAMETERS</span></span>

### <span data-ttu-id="f9800-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f9800-116">-ApiVersion</span></span>
<span data-ttu-id="f9800-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9800-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f9800-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f9800-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f9800-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="f9800-119">-AsJob</span></span>
<span data-ttu-id="f9800-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f9800-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9800-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9800-121">-DefaultProfile</span></span>
<span data-ttu-id="f9800-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9800-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9800-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f9800-123">-Id</span></span>
<span data-ttu-id="f9800-124">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f9800-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f9800-125">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f9800-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9800-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9800-126">-InputObject</span></span>
<span data-ttu-id="f9800-127">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f9800-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9800-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9800-128">-Name</span></span>
<span data-ttu-id="f9800-129">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="f9800-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9800-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f9800-130">-PassThru</span></span>
<span data-ttu-id="f9800-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f9800-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f9800-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f9800-132">-Pre</span></span>
<span data-ttu-id="f9800-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9800-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f9800-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9800-134">-Confirm</span></span>
<span data-ttu-id="f9800-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9800-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9800-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9800-136">-WhatIf</span></span>
<span data-ttu-id="f9800-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9800-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9800-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9800-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9800-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9800-139">CommonParameters</span></span>
<span data-ttu-id="f9800-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9800-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9800-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9800-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9800-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9800-142">INPUTS</span></span>

### <span data-ttu-id="f9800-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f9800-143">System.String</span></span>

## <span data-ttu-id="f9800-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9800-144">OUTPUTS</span></span>

### <span data-ttu-id="f9800-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9800-145">System.Boolean</span></span>

## <span data-ttu-id="f9800-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9800-146">NOTES</span></span>

## <span data-ttu-id="f9800-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9800-147">RELATED LINKS</span></span>
