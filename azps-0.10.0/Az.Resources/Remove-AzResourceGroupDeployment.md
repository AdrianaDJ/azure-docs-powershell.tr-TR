---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: da66d0cacbddbeb53972308faa681bde42c813d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936338"
---
# <span data-ttu-id="275d1-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="275d1-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="275d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275d1-102">SYNOPSIS</span></span>
<span data-ttu-id="275d1-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="275d1-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="275d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="275d1-104">SYNTAX</span></span>

### <span data-ttu-id="275d1-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="275d1-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275d1-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="275d1-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="275d1-107">DESCRIPTION</span></span>
<span data-ttu-id="275d1-108">**Remove-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="275d1-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="275d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="275d1-109">EXAMPLES</span></span>

## <span data-ttu-id="275d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="275d1-110">PARAMETERS</span></span>

### <span data-ttu-id="275d1-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="275d1-111">-ApiVersion</span></span>
<span data-ttu-id="275d1-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="275d1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="275d1-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="275d1-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="275d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275d1-114">-DefaultProfile</span></span>
<span data-ttu-id="275d1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="275d1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275d1-116">-ID</span><span class="sxs-lookup"><span data-stu-id="275d1-116">-Id</span></span>
<span data-ttu-id="275d1-117">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="275d1-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="275d1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="275d1-118">-Name</span></span>
<span data-ttu-id="275d1-119">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="275d1-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275d1-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="275d1-120">-Pre</span></span>
<span data-ttu-id="275d1-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="275d1-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="275d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="275d1-123">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="275d1-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275d1-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="275d1-124">-Confirm</span></span>
<span data-ttu-id="275d1-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="275d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275d1-126">-WhatIf</span></span>
<span data-ttu-id="275d1-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="275d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275d1-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="275d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275d1-129">CommonParameters</span></span>
<span data-ttu-id="275d1-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="275d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275d1-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275d1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275d1-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="275d1-132">INPUTS</span></span>

### <span data-ttu-id="275d1-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="275d1-133">None</span></span>

## <span data-ttu-id="275d1-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="275d1-134">OUTPUTS</span></span>

## <span data-ttu-id="275d1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="275d1-135">NOTES</span></span>

## <span data-ttu-id="275d1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="275d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="275d1-137">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="275d1-137">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="275d1-138">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="275d1-138">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="275d1-139">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="275d1-139">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="275d1-140">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="275d1-140">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


