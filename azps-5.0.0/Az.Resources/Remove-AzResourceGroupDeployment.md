---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279829"
---
# <span data-ttu-id="69110-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="69110-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="69110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69110-102">SYNOPSIS</span></span>
<span data-ttu-id="69110-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69110-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="69110-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69110-104">SYNTAX</span></span>

### <span data-ttu-id="69110-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69110-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69110-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="69110-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69110-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="69110-107">DESCRIPTION</span></span>

<span data-ttu-id="69110-108">**Remove-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69110-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="69110-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69110-109">EXAMPLES</span></span>

### <span data-ttu-id="69110-110">Örnek 1: RESOURCEID ile kaynak grubu dağıtımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="69110-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="69110-111">Bu komut, dağıtımın tam kaynak kimliğiyle kaynak grubu dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69110-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="69110-112">Başarılı kaldırma doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="69110-112">Successful removal returns true.</span></span>

### <span data-ttu-id="69110-113">Örnek 2: ResourceGroupName ve ResourceName ile kaynak grubu dağıtımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="69110-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="69110-114">Bu komut, sağlanan ResourceGroupName ve ResourceName ile kaynak grubu dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69110-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="69110-115">Başarılı kaldırma doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="69110-115">Successful removal returns true.</span></span>

## <span data-ttu-id="69110-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69110-116">PARAMETERS</span></span>

### <span data-ttu-id="69110-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69110-117">-DefaultProfile</span></span>
<span data-ttu-id="69110-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69110-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69110-119">-ID</span><span class="sxs-lookup"><span data-stu-id="69110-119">-Id</span></span>
<span data-ttu-id="69110-120">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="69110-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="69110-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="69110-121">-Name</span></span>
<span data-ttu-id="69110-122">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69110-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="69110-123">-Pre-</span><span class="sxs-lookup"><span data-stu-id="69110-123">-Pre</span></span>
<span data-ttu-id="69110-124">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="69110-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="69110-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69110-125">-ResourceGroupName</span></span>
<span data-ttu-id="69110-126">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69110-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="69110-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="69110-127">-Confirm</span></span>
<span data-ttu-id="69110-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69110-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69110-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69110-129">-WhatIf</span></span>
<span data-ttu-id="69110-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69110-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69110-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69110-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69110-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69110-132">CommonParameters</span></span>
<span data-ttu-id="69110-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69110-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69110-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69110-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69110-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69110-135">INPUTS</span></span>

### <span data-ttu-id="69110-136">System. String</span><span class="sxs-lookup"><span data-stu-id="69110-136">System.String</span></span>

## <span data-ttu-id="69110-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69110-137">OUTPUTS</span></span>

### <span data-ttu-id="69110-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69110-138">System.Boolean</span></span>

## <span data-ttu-id="69110-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69110-139">NOTES</span></span>

## <span data-ttu-id="69110-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69110-140">RELATED LINKS</span></span>

[<span data-ttu-id="69110-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="69110-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="69110-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="69110-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="69110-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="69110-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="69110-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="69110-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


