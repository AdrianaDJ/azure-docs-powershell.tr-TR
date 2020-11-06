---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592556"
---
# <span data-ttu-id="56073-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="56073-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="56073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56073-102">SYNOPSIS</span></span>
<span data-ttu-id="56073-103">Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56073-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56073-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56073-104">SYNTAX</span></span>

### <span data-ttu-id="56073-105">Dağıtım adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="56073-105">The deployment name parameter set.</span></span> <span data-ttu-id="56073-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="56073-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56073-107">Dağıtım kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="56073-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56073-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="56073-108">DESCRIPTION</span></span>
<span data-ttu-id="56073-109">**Remove-AzureRmResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubu dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56073-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="56073-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56073-110">EXAMPLES</span></span>

## <span data-ttu-id="56073-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56073-111">PARAMETERS</span></span>

### <span data-ttu-id="56073-112">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="56073-112">-ApiVersion</span></span>
<span data-ttu-id="56073-113">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="56073-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="56073-114">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="56073-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="56073-115">-ID</span><span class="sxs-lookup"><span data-stu-id="56073-115">-Id</span></span>
<span data-ttu-id="56073-116">Kaldırılacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="56073-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56073-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="56073-117">-Name</span></span>
<span data-ttu-id="56073-118">Kaldırılacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56073-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56073-119">-Pre-</span><span class="sxs-lookup"><span data-stu-id="56073-119">-Pre</span></span>
<span data-ttu-id="56073-120">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="56073-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="56073-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56073-121">-ResourceGroupName</span></span>
<span data-ttu-id="56073-122">Kaldırılacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56073-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56073-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="56073-123">-Confirm</span></span>
<span data-ttu-id="56073-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56073-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56073-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56073-125">-WhatIf</span></span>
<span data-ttu-id="56073-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56073-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56073-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56073-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56073-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56073-128">-DefaultProfile</span></span>
<span data-ttu-id="56073-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56073-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56073-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56073-130">CommonParameters</span></span>
<span data-ttu-id="56073-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56073-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56073-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56073-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56073-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56073-133">INPUTS</span></span>

## <span data-ttu-id="56073-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56073-134">OUTPUTS</span></span>

### <span data-ttu-id="56073-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56073-135">System.Boolean</span></span>

## <span data-ttu-id="56073-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56073-136">NOTES</span></span>

## <span data-ttu-id="56073-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56073-137">RELATED LINKS</span></span>

[<span data-ttu-id="56073-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="56073-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="56073-139">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="56073-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="56073-140">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="56073-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="56073-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="56073-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


