---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266885"
---
# <span data-ttu-id="ef6e9-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ef6e9-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="ef6e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6e9-103">İlke kümesi tanımını değiştirme</span><span class="sxs-lookup"><span data-stu-id="ef6e9-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="ef6e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef6e9-104">SYNTAX</span></span>

### <span data-ttu-id="ef6e9-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef6e9-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6e9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6e9-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6e9-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ef6e9-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6e9-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="ef6e9-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6e9-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="ef6e9-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef6e9-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef6e9-110">DESCRIPTION</span></span>
<span data-ttu-id="ef6e9-111">**Set-AzPolicySetDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="ef6e9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef6e9-112">EXAMPLES</span></span>

### <span data-ttu-id="ef6e9-113">Örnek 1: ilke kümesi tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ef6e9-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="ef6e9-114">İlk komut, Get-AzPolicySetDefinition cmdlet 'ini kullanarak bir ilke kümesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ef6e9-115">Komut bu nesneyi $PolicySetDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="ef6e9-116">İkinci komut $PolicySetDefinition 'un **RESOURCEID** özelliği tarafından tanımlanan ilke kümesi tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="ef6e9-117">Örnek 2: ilke kümesi tanımının meta verilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ef6e9-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="ef6e9-118">Bu komut, VMPolicySetDefinition adındaki bir ilke kümesi tanımının meta verilerini, kategorisinin "sanal makine" olduğunu belirtecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="ef6e9-119">Örnek 3: ilke kümesi tanımının gruplarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ef6e9-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="ef6e9-120">Bu komut, VMPolicySetDefinition adlı bir ilke kümesi tanımının gruplarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="ef6e9-121">Örnek 4: karma tablo kullanarak ilke kümesi tanımının gruplarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ef6e9-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="ef6e9-122">Bu komut, VMPolicySetDefinition adındaki bir ilke kümesi tanımının gruplarını, grup oluşturmak için karma tablo kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="ef6e9-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef6e9-123">PARAMETERS</span></span>

### <span data-ttu-id="ef6e9-124">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ef6e9-124">-ApiVersion</span></span>
<span data-ttu-id="ef6e9-125">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef6e9-126">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ef6e9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6e9-127">-DefaultProfile</span></span>
<span data-ttu-id="ef6e9-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ef6e9-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef6e9-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ef6e9-129">-Description</span></span>
<span data-ttu-id="ef6e9-130">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="ef6e9-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ef6e9-131">-DisplayName</span></span>
<span data-ttu-id="ef6e9-132">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="ef6e9-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="ef6e9-133">-GroupDefinition</span></span>
<span data-ttu-id="ef6e9-134">Güncelleştirilmiş ilke kümesi tanımının ilke tanımı grupları.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="ef6e9-135">Bu, grupları içeren bir dosyanın yolu veya JSON dizesi olarak gruplar olabilir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="ef6e9-136">-ID</span><span class="sxs-lookup"><span data-stu-id="ef6e9-136">-Id</span></span>
<span data-ttu-id="ef6e9-137">Abonelik dahil tam nitelikli ilke tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="ef6e9-138">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="ef6e9-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="ef6e9-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef6e9-139">-InputObject</span></span>
<span data-ttu-id="ef6e9-140">Başka bir cmdlet 'ten çıktı olan güncelleştirilecek ilke kümesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="ef6e9-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6e9-141">-ManagementGroupName</span></span>
<span data-ttu-id="ef6e9-142">Güncelleştirilecek ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="ef6e9-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ef6e9-143">-Metadata</span></span>
<span data-ttu-id="ef6e9-144">Güncelleştirilmiş ilke kümesi tanımının meta verileri.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="ef6e9-145">Bu, meta verileri içeren bir dosya adının yolu veya JSON dizesi olarak meta veri olabilir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="ef6e9-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef6e9-146">-Name</span></span>
<span data-ttu-id="ef6e9-147">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="ef6e9-148">-Parametre</span><span class="sxs-lookup"><span data-stu-id="ef6e9-148">-Parameter</span></span>
<span data-ttu-id="ef6e9-149">Güncelleştirilmiş ilke kümesi tanımının parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="ef6e9-150">Bu, parametre bildirimini içeren bir dosya adı veya URI veya JSON dizesi olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="ef6e9-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef6e9-151">-PolicyDefinition</span></span>
<span data-ttu-id="ef6e9-152">İlke tanımları.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-152">The policy definitions.</span></span> <span data-ttu-id="ef6e9-153">Bu, ilke tanımlarını içeren bir dosya adına veya JSON dizesi olarak ilke tanımlarına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="ef6e9-154">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ef6e9-154">-Pre</span></span>
<span data-ttu-id="ef6e9-155">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ef6e9-156">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ef6e9-156">-SubscriptionId</span></span>
<span data-ttu-id="ef6e9-157">Güncelleştirilecek ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="ef6e9-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef6e9-158">-Confirm</span></span>
<span data-ttu-id="ef6e9-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6e9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6e9-160">-WhatIf</span></span>
<span data-ttu-id="ef6e9-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef6e9-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef6e9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6e9-163">CommonParameters</span></span>
<span data-ttu-id="ef6e9-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6e9-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6e9-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef6e9-166">INPUTS</span></span>

### <span data-ttu-id="ef6e9-167">System. String</span><span class="sxs-lookup"><span data-stu-id="ef6e9-167">System.String</span></span>

### <span data-ttu-id="ef6e9-168">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef6e9-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ef6e9-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef6e9-169">OUTPUTS</span></span>

### <span data-ttu-id="ef6e9-170">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ef6e9-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ef6e9-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef6e9-171">NOTES</span></span>

## <span data-ttu-id="ef6e9-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef6e9-172">RELATED LINKS</span></span>
