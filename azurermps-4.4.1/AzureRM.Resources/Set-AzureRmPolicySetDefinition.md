---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590664"
---
# <span data-ttu-id="9767b-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9767b-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="9767b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9767b-102">SYNOPSIS</span></span>
<span data-ttu-id="9767b-103">İlke kümesi tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="9767b-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9767b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9767b-104">SYNTAX</span></span>

### <span data-ttu-id="9767b-105">İlke kümesi tanım adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="9767b-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="9767b-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="9767b-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9767b-107">İlke kümesi tanım kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="9767b-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9767b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9767b-108">DESCRIPTION</span></span>
<span data-ttu-id="9767b-109">**Set-AzureRmPolicySetDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9767b-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="9767b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9767b-110">EXAMPLES</span></span>

### <span data-ttu-id="9767b-111">Örnek 1: ilke kümesi tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9767b-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="9767b-112">İlk komut, Get-AzureRmPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="9767b-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="9767b-113">Komut bu nesneyi $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9767b-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="9767b-114">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliği tarafından tanımlanan ilke kümesi tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="9767b-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="9767b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9767b-115">PARAMETERS</span></span>

### <span data-ttu-id="9767b-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9767b-116">-ApiVersion</span></span>
<span data-ttu-id="9767b-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="9767b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9767b-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9767b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9767b-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9767b-119">-Description</span></span>
<span data-ttu-id="9767b-120">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9767b-120">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9767b-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9767b-121">-DisplayName</span></span>
<span data-ttu-id="9767b-122">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="9767b-122">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9767b-123">-ID</span><span class="sxs-lookup"><span data-stu-id="9767b-123">-Id</span></span>
<span data-ttu-id="9767b-124">Abonelik dahil tam nitelikli ilke tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="9767b-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="9767b-125">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="9767b-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="9767b-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9767b-126">-Name</span></span>
<span data-ttu-id="9767b-127">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="9767b-127">The policy set definition name.</span></span>

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

### <span data-ttu-id="9767b-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9767b-128">-PolicyDefinition</span></span>
<span data-ttu-id="9767b-129">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="9767b-129">The policy set definition.</span></span> <span data-ttu-id="9767b-130">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="9767b-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9767b-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9767b-131">-Pre</span></span>
<span data-ttu-id="9767b-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9767b-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9767b-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="9767b-133">-Confirm</span></span>
<span data-ttu-id="9767b-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9767b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9767b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9767b-135">-DefaultProfile</span></span>
<span data-ttu-id="9767b-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9767b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9767b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9767b-137">-WhatIf</span></span>
<span data-ttu-id="9767b-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9767b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9767b-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9767b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9767b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9767b-140">CommonParameters</span></span>
<span data-ttu-id="9767b-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9767b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9767b-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9767b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9767b-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9767b-143">INPUTS</span></span>

### <span data-ttu-id="9767b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9767b-144">System.String</span></span>

## <span data-ttu-id="9767b-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9767b-145">OUTPUTS</span></span>

### <span data-ttu-id="9767b-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9767b-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9767b-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9767b-147">NOTES</span></span>

## <span data-ttu-id="9767b-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9767b-148">RELATED LINKS</span></span>

