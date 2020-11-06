---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591620"
---
# <span data-ttu-id="213ba-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="213ba-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="213ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="213ba-102">SYNOPSIS</span></span>
<span data-ttu-id="213ba-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="213ba-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="213ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="213ba-104">SYNTAX</span></span>

### <span data-ttu-id="213ba-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="213ba-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213ba-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="213ba-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="213ba-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="213ba-107">DESCRIPTION</span></span>
<span data-ttu-id="213ba-108">**Remove-AzureRmResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="213ba-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="213ba-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="213ba-109">EXAMPLES</span></span>

## <span data-ttu-id="213ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="213ba-110">PARAMETERS</span></span>

### <span data-ttu-id="213ba-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="213ba-111">-ApiVersion</span></span>
<span data-ttu-id="213ba-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="213ba-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="213ba-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="213ba-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="213ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213ba-114">-DefaultProfile</span></span>
<span data-ttu-id="213ba-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="213ba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="213ba-116">-ID</span><span class="sxs-lookup"><span data-stu-id="213ba-116">-Id</span></span>
<span data-ttu-id="213ba-117">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="213ba-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213ba-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="213ba-118">-Name</span></span>
<span data-ttu-id="213ba-119">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="213ba-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213ba-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="213ba-120">-Pre</span></span>
<span data-ttu-id="213ba-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="213ba-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="213ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="213ba-123">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="213ba-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213ba-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="213ba-124">-Confirm</span></span>
<span data-ttu-id="213ba-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="213ba-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213ba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="213ba-126">-WhatIf</span></span>
<span data-ttu-id="213ba-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="213ba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="213ba-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="213ba-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213ba-129">CommonParameters</span></span>
<span data-ttu-id="213ba-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="213ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213ba-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="213ba-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213ba-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="213ba-132">INPUTS</span></span>

### <span data-ttu-id="213ba-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="213ba-133">None</span></span>
<span data-ttu-id="213ba-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="213ba-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="213ba-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="213ba-135">OUTPUTS</span></span>

### <span data-ttu-id="213ba-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="213ba-136">System.Boolean</span></span>

## <span data-ttu-id="213ba-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="213ba-137">NOTES</span></span>

## <span data-ttu-id="213ba-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="213ba-138">RELATED LINKS</span></span>

[<span data-ttu-id="213ba-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="213ba-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="213ba-140">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="213ba-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="213ba-141">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="213ba-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="213ba-142">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="213ba-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


