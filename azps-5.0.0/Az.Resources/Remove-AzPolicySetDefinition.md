---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279840"
---
# <span data-ttu-id="c37ca-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c37ca-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c37ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c37ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c37ca-103">İlke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c37ca-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="c37ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c37ca-104">SYNTAX</span></span>

### <span data-ttu-id="c37ca-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c37ca-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37ca-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c37ca-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37ca-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c37ca-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37ca-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="c37ca-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37ca-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c37ca-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c37ca-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="c37ca-110">DESCRIPTION</span></span>
<span data-ttu-id="c37ca-111">**Remove-AzPolicySetDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c37ca-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="c37ca-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c37ca-112">EXAMPLES</span></span>

### <span data-ttu-id="c37ca-113">Örnek 1: kaynak KIMLIĞIYLE ilke kümesi tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c37ca-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="c37ca-114">İlk komut, Get-AzPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="c37ca-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="c37ca-115">Komut, $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c37ca-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="c37ca-116">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliğinin tanımladığı ilke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c37ca-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="c37ca-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c37ca-117">PARAMETERS</span></span>

### <span data-ttu-id="c37ca-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c37ca-118">-ApiVersion</span></span>
<span data-ttu-id="c37ca-119">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="c37ca-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c37ca-120">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c37ca-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c37ca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37ca-121">-DefaultProfile</span></span>
<span data-ttu-id="c37ca-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c37ca-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c37ca-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c37ca-123">-Force</span></span>
<span data-ttu-id="c37ca-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c37ca-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c37ca-125">-ID</span><span class="sxs-lookup"><span data-stu-id="c37ca-125">-Id</span></span>
<span data-ttu-id="c37ca-126">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="c37ca-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="c37ca-127">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="c37ca-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37ca-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c37ca-128">-InputObject</span></span>
<span data-ttu-id="c37ca-129">Başka bir cmdlet 'ten çıktı olan kaldırılacak ilke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c37ca-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c37ca-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c37ca-130">-ManagementGroupName</span></span>
<span data-ttu-id="c37ca-131">Silinecek ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c37ca-131">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37ca-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="c37ca-132">-Name</span></span>
<span data-ttu-id="c37ca-133">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="c37ca-133">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37ca-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c37ca-134">-Pre</span></span>
<span data-ttu-id="c37ca-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c37ca-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c37ca-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c37ca-136">-SubscriptionId</span></span>
<span data-ttu-id="c37ca-137">Silinecek ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c37ca-137">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37ca-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="c37ca-138">-Confirm</span></span>
<span data-ttu-id="c37ca-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c37ca-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c37ca-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c37ca-140">-WhatIf</span></span>
<span data-ttu-id="c37ca-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c37ca-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c37ca-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c37ca-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c37ca-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37ca-143">CommonParameters</span></span>
<span data-ttu-id="c37ca-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c37ca-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37ca-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c37ca-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37ca-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c37ca-146">INPUTS</span></span>

### <span data-ttu-id="c37ca-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c37ca-147">System.String</span></span>

### <span data-ttu-id="c37ca-148">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c37ca-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c37ca-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c37ca-149">OUTPUTS</span></span>

### <span data-ttu-id="c37ca-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c37ca-150">System.Boolean</span></span>

## <span data-ttu-id="c37ca-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c37ca-151">NOTES</span></span>

## <span data-ttu-id="c37ca-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c37ca-152">RELATED LINKS</span></span>
