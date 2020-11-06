---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591624"
---
# <span data-ttu-id="ee1ab-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ee1ab-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="ee1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1ab-103">İlke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee1ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee1ab-104">SYNTAX</span></span>

### <span data-ttu-id="ee1ab-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee1ab-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1ab-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="ee1ab-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1ab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee1ab-107">DESCRIPTION</span></span>
<span data-ttu-id="ee1ab-108">**Remove-AzureRmPolicySetDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ee1ab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee1ab-109">EXAMPLES</span></span>

### <span data-ttu-id="ee1ab-110">Örnek 1: kaynak KIMLIĞIYLE ilke kümesi tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ee1ab-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="ee1ab-111">İlk komut, Get-AzureRmPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ee1ab-112">Komut, $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="ee1ab-113">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliğinin tanımladığı ilke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="ee1ab-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee1ab-114">PARAMETERS</span></span>

### <span data-ttu-id="ee1ab-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ee1ab-115">-ApiVersion</span></span>
<span data-ttu-id="ee1ab-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ee1ab-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ee1ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1ab-118">-DefaultProfile</span></span>
<span data-ttu-id="ee1ab-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee1ab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee1ab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ee1ab-120">-Force</span></span>
<span data-ttu-id="ee1ab-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ee1ab-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ee1ab-122">-Id</span></span>
<span data-ttu-id="ee1ab-123">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ee1ab-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="ee1ab-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1ab-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee1ab-125">-Name</span></span>
<span data-ttu-id="ee1ab-126">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1ab-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ee1ab-127">-Pre</span></span>
<span data-ttu-id="ee1ab-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ee1ab-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee1ab-129">-Confirm</span></span>
<span data-ttu-id="ee1ab-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1ab-131">-WhatIf</span></span>
<span data-ttu-id="ee1ab-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1ab-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1ab-134">CommonParameters</span></span>
<span data-ttu-id="ee1ab-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1ab-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1ab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1ab-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee1ab-137">INPUTS</span></span>

### <span data-ttu-id="ee1ab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ee1ab-138">System.String</span></span>

## <span data-ttu-id="ee1ab-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee1ab-139">OUTPUTS</span></span>

### <span data-ttu-id="ee1ab-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee1ab-140">System.Boolean</span></span>

## <span data-ttu-id="ee1ab-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee1ab-141">NOTES</span></span>

## <span data-ttu-id="ee1ab-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee1ab-142">RELATED LINKS</span></span>
