---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 19662972e115acb0e3a194e14abf3f956d39035e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589364"
---
# <span data-ttu-id="8560c-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8560c-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8560c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8560c-102">SYNOPSIS</span></span>
<span data-ttu-id="8560c-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8560c-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8560c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8560c-104">SYNTAX</span></span>

### <span data-ttu-id="8560c-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8560c-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8560c-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8560c-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8560c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8560c-107">DESCRIPTION</span></span>
<span data-ttu-id="8560c-108">**Remove-AzureRmResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8560c-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="8560c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8560c-109">EXAMPLES</span></span>

## <span data-ttu-id="8560c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8560c-110">PARAMETERS</span></span>

### <span data-ttu-id="8560c-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8560c-111">-ApiVersion</span></span>
<span data-ttu-id="8560c-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8560c-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8560c-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8560c-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8560c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8560c-114">-DefaultProfile</span></span>
<span data-ttu-id="8560c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8560c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8560c-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8560c-116">-Id</span></span>
<span data-ttu-id="8560c-117">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8560c-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="8560c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8560c-118">-Name</span></span>
<span data-ttu-id="8560c-119">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8560c-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="8560c-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8560c-120">-Pre</span></span>
<span data-ttu-id="8560c-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8560c-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8560c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8560c-122">-ResourceGroupName</span></span>
<span data-ttu-id="8560c-123">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8560c-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="8560c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="8560c-124">-Confirm</span></span>
<span data-ttu-id="8560c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8560c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8560c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8560c-126">-WhatIf</span></span>
<span data-ttu-id="8560c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8560c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8560c-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8560c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8560c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8560c-129">CommonParameters</span></span>
<span data-ttu-id="8560c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8560c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8560c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8560c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8560c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8560c-132">INPUTS</span></span>

### <span data-ttu-id="8560c-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8560c-133">None</span></span>

## <span data-ttu-id="8560c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8560c-134">OUTPUTS</span></span>

## <span data-ttu-id="8560c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8560c-135">NOTES</span></span>

## <span data-ttu-id="8560c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8560c-136">RELATED LINKS</span></span>

[<span data-ttu-id="8560c-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8560c-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8560c-138">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8560c-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8560c-139">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8560c-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8560c-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8560c-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


