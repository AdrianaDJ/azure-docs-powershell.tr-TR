---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097212"
---
# <span data-ttu-id="f386d-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f386d-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="f386d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f386d-102">SYNOPSIS</span></span>
<span data-ttu-id="f386d-103">İlke kümesi tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="f386d-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="f386d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f386d-104">SYNTAX</span></span>

### <span data-ttu-id="f386d-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f386d-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f386d-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f386d-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f386d-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f386d-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f386d-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="f386d-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f386d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f386d-109">DESCRIPTION</span></span>
<span data-ttu-id="f386d-110">**Set-AzPolicySetDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f386d-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f386d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f386d-111">EXAMPLES</span></span>

### <span data-ttu-id="f386d-112">Örnek 1: ilke kümesi tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f386d-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f386d-113">İlk komut, Get-AzPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="f386d-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f386d-114">Komut bu nesneyi $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f386d-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="f386d-115">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliği tarafından tanımlanan ilke kümesi tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="f386d-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="f386d-116">Örnek 2: ilke kümesi tanımının meta verilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f386d-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="f386d-117">Bu komut, VMPolicySetDefinition adındaki bir ilke kümesi tanımının meta verilerini, kategorisinin "sanal makine" olduğunu belirtecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f386d-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="f386d-118">Örnek 3: ilke kümesi tanımının gruplarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f386d-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="f386d-119">Bu komut, VMPolicySetDefinition adlı bir ilke kümesi tanımının gruplarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f386d-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="f386d-120">Örnek 4: karma tablo kullanarak ilke kümesi tanımının gruplarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f386d-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="f386d-121">Bu komut, VMPolicySetDefinition adındaki bir ilke kümesi tanımının gruplarını, grup oluşturmak için karma tablo kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f386d-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="f386d-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f386d-122">PARAMETERS</span></span>

### <span data-ttu-id="f386d-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f386d-123">-ApiVersion</span></span>
<span data-ttu-id="f386d-124">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f386d-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f386d-125">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f386d-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f386d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f386d-126">-DefaultProfile</span></span>
<span data-ttu-id="f386d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f386d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f386d-128">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f386d-128">-Description</span></span>
<span data-ttu-id="f386d-129">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="f386d-129">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f386d-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f386d-130">-DisplayName</span></span>
<span data-ttu-id="f386d-131">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="f386d-131">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f386d-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="f386d-132">-GroupDefinition</span></span>
<span data-ttu-id="f386d-133">Güncelleştirilmiş ilke kümesi tanımının ilke tanımı grupları.</span><span class="sxs-lookup"><span data-stu-id="f386d-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="f386d-134">Bu, grupları içeren bir dosyanın yolu veya JSON dizesi olarak gruplar olabilir.</span><span class="sxs-lookup"><span data-stu-id="f386d-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="f386d-135">-ID</span><span class="sxs-lookup"><span data-stu-id="f386d-135">-Id</span></span>
<span data-ttu-id="f386d-136">Abonelik dahil tam nitelikli ilke tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="f386d-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="f386d-137">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="f386d-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="f386d-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f386d-138">-ManagementGroupName</span></span>
<span data-ttu-id="f386d-139">Güncelleştirilecek ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f386d-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="f386d-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f386d-140">-Metadata</span></span>
<span data-ttu-id="f386d-141">Güncelleştirilmiş ilke kümesi tanımının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="f386d-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="f386d-142">Bu, meta verileri içeren bir dosya adının yolu veya JSON dizesi olarak meta veri olabilir.</span><span class="sxs-lookup"><span data-stu-id="f386d-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="f386d-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="f386d-143">-Name</span></span>
<span data-ttu-id="f386d-144">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="f386d-144">The policy set definition name.</span></span>

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

### <span data-ttu-id="f386d-145">-Parametre</span><span class="sxs-lookup"><span data-stu-id="f386d-145">-Parameter</span></span>
<span data-ttu-id="f386d-146">Güncelleştirilmiş ilke kümesi tanımının parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="f386d-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="f386d-147">Bu, parametre bildirimini içeren bir dosya adı veya URI veya JSON dizesi olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="f386d-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="f386d-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f386d-148">-PolicyDefinition</span></span>
<span data-ttu-id="f386d-149">İlke tanımları.</span><span class="sxs-lookup"><span data-stu-id="f386d-149">The policy definitions.</span></span> <span data-ttu-id="f386d-150">Bu, ilke tanımlarını içeren bir dosya adına veya JSON dizesi olarak ilke tanımlarına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="f386d-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="f386d-151">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f386d-151">-Pre</span></span>
<span data-ttu-id="f386d-152">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f386d-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f386d-153">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f386d-153">-SubscriptionId</span></span>
<span data-ttu-id="f386d-154">Güncelleştirilecek ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f386d-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="f386d-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="f386d-155">-Confirm</span></span>
<span data-ttu-id="f386d-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f386d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f386d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f386d-157">-WhatIf</span></span>
<span data-ttu-id="f386d-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f386d-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f386d-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f386d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f386d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f386d-160">CommonParameters</span></span>
<span data-ttu-id="f386d-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f386d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f386d-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f386d-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f386d-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f386d-163">INPUTS</span></span>

### <span data-ttu-id="f386d-164">System. String</span><span class="sxs-lookup"><span data-stu-id="f386d-164">System.String</span></span>

### <span data-ttu-id="f386d-165">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="f386d-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f386d-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f386d-166">OUTPUTS</span></span>

### <span data-ttu-id="f386d-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f386d-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f386d-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f386d-168">NOTES</span></span>

## <span data-ttu-id="f386d-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f386d-169">RELATED LINKS</span></span>
