---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573289"
---
# <span data-ttu-id="ffe7c-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ffe7c-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="ffe7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffe7c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe7c-103">İlke kümesi tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="ffe7c-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffe7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffe7c-104">SYNTAX</span></span>

### <span data-ttu-id="ffe7c-105">Setbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ffe7c-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe7c-106">Setbyıd</span><span class="sxs-lookup"><span data-stu-id="ffe7c-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffe7c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffe7c-107">DESCRIPTION</span></span>
<span data-ttu-id="ffe7c-108">**Set-AzureRmPolicySetDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="ffe7c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffe7c-109">EXAMPLES</span></span>

### <span data-ttu-id="ffe7c-110">Örnek 1: ilke kümesi tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ffe7c-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="ffe7c-111">İlk komut, Get-AzureRmPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ffe7c-112">Komut bu nesneyi $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="ffe7c-113">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliği tarafından tanımlanan ilke kümesi tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="ffe7c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffe7c-114">PARAMETERS</span></span>

### <span data-ttu-id="ffe7c-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ffe7c-115">-ApiVersion</span></span>
<span data-ttu-id="ffe7c-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ffe7c-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ffe7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe7c-118">-DefaultProfile</span></span>
<span data-ttu-id="ffe7c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ffe7c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffe7c-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ffe7c-120">-Description</span></span>
<span data-ttu-id="ffe7c-121">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ffe7c-122">-DisplayName</span></span>
<span data-ttu-id="ffe7c-123">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7c-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ffe7c-124">-Id</span></span>
<span data-ttu-id="ffe7c-125">Abonelik dahil tam nitelikli ilke tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="ffe7c-126">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="ffe7c-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffe7c-127">-Name</span></span>
<span data-ttu-id="ffe7c-128">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7c-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ffe7c-129">-PolicyDefinition</span></span>
<span data-ttu-id="ffe7c-130">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-130">The policy set definition.</span></span> <span data-ttu-id="ffe7c-131">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7c-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ffe7c-132">-Pre</span></span>
<span data-ttu-id="ffe7c-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ffe7c-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffe7c-134">-Confirm</span></span>
<span data-ttu-id="ffe7c-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffe7c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffe7c-136">-WhatIf</span></span>
<span data-ttu-id="ffe7c-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffe7c-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffe7c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe7c-139">CommonParameters</span></span>
<span data-ttu-id="ffe7c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffe7c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe7c-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe7c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe7c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffe7c-142">INPUTS</span></span>

### <span data-ttu-id="ffe7c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ffe7c-143">System.String</span></span>

## <span data-ttu-id="ffe7c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffe7c-144">OUTPUTS</span></span>

### <span data-ttu-id="ffe7c-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ffe7c-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ffe7c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffe7c-146">NOTES</span></span>

## <span data-ttu-id="ffe7c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffe7c-147">RELATED LINKS</span></span>
