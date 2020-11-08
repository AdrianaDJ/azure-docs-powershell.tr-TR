---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933299"
---
# <span data-ttu-id="394be-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="394be-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="394be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394be-102">SYNOPSIS</span></span>
<span data-ttu-id="394be-103">İlke kümesi tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="394be-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="394be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="394be-104">SYNTAX</span></span>

### <span data-ttu-id="394be-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="394be-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="394be-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="394be-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="394be-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="394be-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="394be-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="394be-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="394be-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="394be-109">DESCRIPTION</span></span>
<span data-ttu-id="394be-110">**Set-AzPolicySetDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="394be-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="394be-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="394be-111">EXAMPLES</span></span>

### <span data-ttu-id="394be-112">Örnek 1: ilke kümesi tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="394be-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="394be-113">İlk komut, Get-AzPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="394be-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="394be-114">Komut bu nesneyi $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="394be-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="394be-115">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliği tarafından tanımlanan ilke kümesi tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="394be-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="394be-116">Örnek 2: ilke kümesi tanımının meta verilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="394be-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="394be-117">Bu komut, VMPolicySetDefinition adındaki bir ilke kümesi tanımının meta verilerini, kategorisinin "sanal makine" olduğunu belirtecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="394be-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="394be-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="394be-118">PARAMETERS</span></span>

### <span data-ttu-id="394be-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="394be-119">-ApiVersion</span></span>
<span data-ttu-id="394be-120">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="394be-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="394be-121">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="394be-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="394be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394be-122">-DefaultProfile</span></span>
<span data-ttu-id="394be-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="394be-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="394be-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="394be-124">-Description</span></span>
<span data-ttu-id="394be-125">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="394be-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="394be-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="394be-126">-DisplayName</span></span>
<span data-ttu-id="394be-127">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="394be-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="394be-128">-ID</span><span class="sxs-lookup"><span data-stu-id="394be-128">-Id</span></span>
<span data-ttu-id="394be-129">Abonelik dahil tam nitelikli ilke tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="394be-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="394be-130">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="394be-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="394be-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="394be-131">-ManagementGroupName</span></span>
<span data-ttu-id="394be-132">Güncelleştirilecek ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="394be-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="394be-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="394be-133">-Metadata</span></span>
<span data-ttu-id="394be-134">Güncelleştirilmiş ilke kümesi tanımının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="394be-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="394be-135">Bu, meta veri içeren bir dosya adı veya meta veri içeren bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="394be-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="394be-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="394be-136">-Name</span></span>
<span data-ttu-id="394be-137">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="394be-137">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394be-138">-Parametre</span><span class="sxs-lookup"><span data-stu-id="394be-138">-Parameter</span></span>
<span data-ttu-id="394be-139">Güncelleştirilmiş ilke kümesi tanımının parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="394be-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="394be-140">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="394be-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="394be-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="394be-141">-PolicyDefinition</span></span>
<span data-ttu-id="394be-142">İlke tanımları.</span><span class="sxs-lookup"><span data-stu-id="394be-142">The policy definitions.</span></span> <span data-ttu-id="394be-143">Bu, ilke tanımlarını içeren bir dosya adına veya dizi olarak ilke tanımlarına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="394be-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="394be-144">-Pre-</span><span class="sxs-lookup"><span data-stu-id="394be-144">-Pre</span></span>
<span data-ttu-id="394be-145">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="394be-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="394be-146">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="394be-146">-SubscriptionId</span></span>
<span data-ttu-id="394be-147">Güncelleştirilecek ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="394be-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="394be-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="394be-148">-Confirm</span></span>
<span data-ttu-id="394be-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="394be-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="394be-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="394be-150">-WhatIf</span></span>
<span data-ttu-id="394be-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="394be-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="394be-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="394be-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="394be-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394be-153">CommonParameters</span></span>
<span data-ttu-id="394be-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="394be-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394be-155">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="394be-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394be-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="394be-156">INPUTS</span></span>

### <span data-ttu-id="394be-157">System. String</span><span class="sxs-lookup"><span data-stu-id="394be-157">System.String</span></span>

### <span data-ttu-id="394be-158">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="394be-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="394be-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="394be-159">OUTPUTS</span></span>

### <span data-ttu-id="394be-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="394be-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="394be-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="394be-161">NOTES</span></span>

## <span data-ttu-id="394be-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="394be-162">RELATED LINKS</span></span>