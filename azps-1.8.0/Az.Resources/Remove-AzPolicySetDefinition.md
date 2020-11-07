---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 3174f56a0488b196dc3dc330cfa6435def73476c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759336"
---
# <span data-ttu-id="b53c4-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b53c4-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="b53c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b53c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b53c4-103">İlke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b53c4-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="b53c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b53c4-104">SYNTAX</span></span>

### <span data-ttu-id="b53c4-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b53c4-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b53c4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b53c4-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b53c4-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b53c4-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b53c4-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="b53c4-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b53c4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b53c4-109">DESCRIPTION</span></span>
<span data-ttu-id="b53c4-110">**Remove-AzPolicySetDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b53c4-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b53c4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b53c4-111">EXAMPLES</span></span>

### <span data-ttu-id="b53c4-112">Örnek 1: kaynak KIMLIĞIYLE ilke kümesi tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b53c4-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="b53c4-113">İlk komut, Get-AzPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="b53c4-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b53c4-114">Komut, $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b53c4-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="b53c4-115">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliğinin tanımladığı ilke kümesi tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b53c4-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b53c4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b53c4-116">PARAMETERS</span></span>

### <span data-ttu-id="b53c4-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b53c4-117">-ApiVersion</span></span>
<span data-ttu-id="b53c4-118">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="b53c4-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b53c4-119">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b53c4-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b53c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53c4-120">-DefaultProfile</span></span>
<span data-ttu-id="b53c4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b53c4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b53c4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b53c4-122">-Force</span></span>
<span data-ttu-id="b53c4-123">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="b53c4-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b53c4-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b53c4-124">-Id</span></span>
<span data-ttu-id="b53c4-125">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="b53c4-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="b53c4-126">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="b53c4-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b53c4-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b53c4-127">-ManagementGroupName</span></span>
<span data-ttu-id="b53c4-128">Silinecek ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b53c4-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="b53c4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b53c4-129">-Name</span></span>
<span data-ttu-id="b53c4-130">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="b53c4-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="b53c4-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b53c4-131">-Pre</span></span>
<span data-ttu-id="b53c4-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b53c4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b53c4-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b53c4-133">-SubscriptionId</span></span>
<span data-ttu-id="b53c4-134">Silinecek ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b53c4-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="b53c4-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="b53c4-135">-Confirm</span></span>
<span data-ttu-id="b53c4-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b53c4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b53c4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b53c4-137">-WhatIf</span></span>
<span data-ttu-id="b53c4-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b53c4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b53c4-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b53c4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b53c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53c4-140">CommonParameters</span></span>
<span data-ttu-id="b53c4-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b53c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53c4-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53c4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53c4-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b53c4-143">INPUTS</span></span>

### <span data-ttu-id="b53c4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b53c4-144">System.String</span></span>

### <span data-ttu-id="b53c4-145">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b53c4-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b53c4-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b53c4-146">OUTPUTS</span></span>

### <span data-ttu-id="b53c4-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b53c4-147">System.Boolean</span></span>

## <span data-ttu-id="b53c4-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b53c4-148">NOTES</span></span>

## <span data-ttu-id="b53c4-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b53c4-149">RELATED LINKS</span></span>
