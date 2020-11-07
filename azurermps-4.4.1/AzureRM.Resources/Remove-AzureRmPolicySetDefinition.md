---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763326"
---
# <span data-ttu-id="af9dc-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="af9dc-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="af9dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="af9dc-103">İlke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af9dc-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af9dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af9dc-104">SYNTAX</span></span>

### <span data-ttu-id="af9dc-105">İlke kümesi tanım adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="af9dc-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="af9dc-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="af9dc-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9dc-107">İlke kümesi tanım kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="af9dc-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9dc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="af9dc-108">DESCRIPTION</span></span>
<span data-ttu-id="af9dc-109">**Remove-AzureRmPolicySetDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af9dc-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="af9dc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af9dc-110">EXAMPLES</span></span>

### <span data-ttu-id="af9dc-111">Örnek 1: kaynak KIMLIĞIYLE ilke kümesi tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="af9dc-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="af9dc-112">İlk komut, Get-AzureRmPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="af9dc-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="af9dc-113">Komut, $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="af9dc-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="af9dc-114">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliğinin tanımladığı ilke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af9dc-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="af9dc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af9dc-115">PARAMETERS</span></span>

### <span data-ttu-id="af9dc-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="af9dc-116">-ApiVersion</span></span>
<span data-ttu-id="af9dc-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="af9dc-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="af9dc-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af9dc-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="af9dc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="af9dc-119">-Force</span></span>
<span data-ttu-id="af9dc-120">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="af9dc-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="af9dc-121">-ID</span><span class="sxs-lookup"><span data-stu-id="af9dc-121">-Id</span></span>
<span data-ttu-id="af9dc-122">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="af9dc-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="af9dc-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="af9dc-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af9dc-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="af9dc-124">-Name</span></span>
<span data-ttu-id="af9dc-125">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="af9dc-125">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af9dc-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="af9dc-126">-Pre</span></span>
<span data-ttu-id="af9dc-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af9dc-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="af9dc-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="af9dc-128">-Confirm</span></span>
<span data-ttu-id="af9dc-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af9dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9dc-130">-WhatIf</span></span>
<span data-ttu-id="af9dc-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af9dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9dc-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af9dc-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9dc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9dc-133">-DefaultProfile</span></span>
<span data-ttu-id="af9dc-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af9dc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af9dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9dc-135">CommonParameters</span></span>
<span data-ttu-id="af9dc-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af9dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9dc-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9dc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9dc-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af9dc-138">INPUTS</span></span>

### <span data-ttu-id="af9dc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="af9dc-139">System.String</span></span>

## <span data-ttu-id="af9dc-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af9dc-140">OUTPUTS</span></span>

### <span data-ttu-id="af9dc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af9dc-141">System.Boolean</span></span>

## <span data-ttu-id="af9dc-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af9dc-142">NOTES</span></span>

## <span data-ttu-id="af9dc-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af9dc-143">RELATED LINKS</span></span>

