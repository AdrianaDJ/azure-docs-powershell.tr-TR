---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932541"
---
# <span data-ttu-id="97734-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="97734-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="97734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97734-102">SYNOPSIS</span></span>
<span data-ttu-id="97734-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="97734-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="97734-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97734-104">SYNTAX</span></span>

### <span data-ttu-id="97734-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97734-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97734-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="97734-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97734-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97734-107">DESCRIPTION</span></span>
<span data-ttu-id="97734-108">**Remove-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="97734-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="97734-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97734-109">EXAMPLES</span></span>

## <span data-ttu-id="97734-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97734-110">PARAMETERS</span></span>

### <span data-ttu-id="97734-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="97734-111">-ApiVersion</span></span>
<span data-ttu-id="97734-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97734-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="97734-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97734-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="97734-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97734-114">-DefaultProfile</span></span>
<span data-ttu-id="97734-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97734-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97734-116">-ID</span><span class="sxs-lookup"><span data-stu-id="97734-116">-Id</span></span>
<span data-ttu-id="97734-117">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="97734-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="97734-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="97734-118">-Name</span></span>
<span data-ttu-id="97734-119">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97734-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="97734-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="97734-120">-Pre</span></span>
<span data-ttu-id="97734-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="97734-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="97734-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97734-122">-ResourceGroupName</span></span>
<span data-ttu-id="97734-123">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97734-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="97734-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="97734-124">-Confirm</span></span>
<span data-ttu-id="97734-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97734-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97734-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97734-126">-WhatIf</span></span>
<span data-ttu-id="97734-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97734-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97734-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97734-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97734-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97734-129">CommonParameters</span></span>
<span data-ttu-id="97734-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97734-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97734-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97734-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97734-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97734-132">INPUTS</span></span>

### <span data-ttu-id="97734-133">System. String</span><span class="sxs-lookup"><span data-stu-id="97734-133">System.String</span></span>

## <span data-ttu-id="97734-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97734-134">OUTPUTS</span></span>

### <span data-ttu-id="97734-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97734-135">System.Boolean</span></span>

## <span data-ttu-id="97734-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97734-136">NOTES</span></span>

## <span data-ttu-id="97734-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97734-137">RELATED LINKS</span></span>

[<span data-ttu-id="97734-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="97734-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="97734-139">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="97734-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="97734-140">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="97734-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="97734-141">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="97734-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


