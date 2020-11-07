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
ms.locfileid: "93759332"
---
# <span data-ttu-id="26eee-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eee-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="26eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26eee-102">SYNOPSIS</span></span>
<span data-ttu-id="26eee-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26eee-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="26eee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26eee-104">SYNTAX</span></span>

### <span data-ttu-id="26eee-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26eee-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26eee-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="26eee-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26eee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26eee-107">DESCRIPTION</span></span>
<span data-ttu-id="26eee-108">**Remove-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26eee-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="26eee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26eee-109">EXAMPLES</span></span>

## <span data-ttu-id="26eee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26eee-110">PARAMETERS</span></span>

### <span data-ttu-id="26eee-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="26eee-111">-ApiVersion</span></span>
<span data-ttu-id="26eee-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="26eee-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="26eee-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26eee-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="26eee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26eee-114">-DefaultProfile</span></span>
<span data-ttu-id="26eee-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="26eee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26eee-116">-ID</span><span class="sxs-lookup"><span data-stu-id="26eee-116">-Id</span></span>
<span data-ttu-id="26eee-117">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="26eee-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="26eee-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="26eee-118">-Name</span></span>
<span data-ttu-id="26eee-119">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26eee-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="26eee-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="26eee-120">-Pre</span></span>
<span data-ttu-id="26eee-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="26eee-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26eee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26eee-122">-ResourceGroupName</span></span>
<span data-ttu-id="26eee-123">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26eee-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="26eee-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="26eee-124">-Confirm</span></span>
<span data-ttu-id="26eee-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26eee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26eee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26eee-126">-WhatIf</span></span>
<span data-ttu-id="26eee-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26eee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26eee-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26eee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26eee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26eee-129">CommonParameters</span></span>
<span data-ttu-id="26eee-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26eee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26eee-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26eee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26eee-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26eee-132">INPUTS</span></span>

### <span data-ttu-id="26eee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="26eee-133">System.String</span></span>

## <span data-ttu-id="26eee-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26eee-134">OUTPUTS</span></span>

### <span data-ttu-id="26eee-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26eee-135">System.Boolean</span></span>

## <span data-ttu-id="26eee-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26eee-136">NOTES</span></span>

## <span data-ttu-id="26eee-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26eee-137">RELATED LINKS</span></span>

[<span data-ttu-id="26eee-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eee-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="26eee-139">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eee-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="26eee-140">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eee-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="26eee-141">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26eee-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


