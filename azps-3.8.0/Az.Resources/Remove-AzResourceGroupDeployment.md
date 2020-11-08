---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097232"
---
# <span data-ttu-id="ec80e-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec80e-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ec80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec80e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec80e-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec80e-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ec80e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec80e-104">SYNTAX</span></span>

### <span data-ttu-id="ec80e-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec80e-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec80e-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ec80e-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec80e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec80e-107">DESCRIPTION</span></span>

<span data-ttu-id="ec80e-108">**Remove-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec80e-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ec80e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec80e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec80e-110">Örnek 1: RESOURCEID ile kaynak grubu dağıtımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="ec80e-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="ec80e-111">Bu komut, dağıtımın tam kaynak kimliğiyle kaynak grubu dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec80e-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ec80e-112">Başarılı kaldırma doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec80e-112">Successful removal returns true.</span></span>

### <span data-ttu-id="ec80e-113">Örnek 2: ResourceGroupName ve ResourceName ile kaynak grubu dağıtımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="ec80e-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="ec80e-114">Bu komut, sağlanan ResourceGroupName ve ResourceName ile kaynak grubu dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec80e-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="ec80e-115">Başarılı kaldırma doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec80e-115">Successful removal returns true.</span></span>

## <span data-ttu-id="ec80e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec80e-116">PARAMETERS</span></span>

### <span data-ttu-id="ec80e-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ec80e-117">-ApiVersion</span></span>
<span data-ttu-id="ec80e-118">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec80e-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ec80e-119">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec80e-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ec80e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec80e-120">-DefaultProfile</span></span>
<span data-ttu-id="ec80e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ec80e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec80e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ec80e-122">-Id</span></span>
<span data-ttu-id="ec80e-123">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec80e-123">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec80e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec80e-124">-Name</span></span>
<span data-ttu-id="ec80e-125">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec80e-125">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec80e-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ec80e-126">-Pre</span></span>
<span data-ttu-id="ec80e-127">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec80e-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ec80e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec80e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec80e-129">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec80e-129">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec80e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec80e-130">-Confirm</span></span>
<span data-ttu-id="ec80e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec80e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec80e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec80e-132">-WhatIf</span></span>
<span data-ttu-id="ec80e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec80e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec80e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec80e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec80e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec80e-135">CommonParameters</span></span>
<span data-ttu-id="ec80e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec80e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec80e-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec80e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec80e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec80e-138">INPUTS</span></span>

### <span data-ttu-id="ec80e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ec80e-139">System.String</span></span>

## <span data-ttu-id="ec80e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec80e-140">OUTPUTS</span></span>

### <span data-ttu-id="ec80e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec80e-141">System.Boolean</span></span>

## <span data-ttu-id="ec80e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec80e-142">NOTES</span></span>

## <span data-ttu-id="ec80e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec80e-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec80e-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec80e-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ec80e-145">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec80e-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ec80e-146">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec80e-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="ec80e-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec80e-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


