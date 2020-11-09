---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322118"
---
# <span data-ttu-id="9b41d-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9b41d-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="9b41d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b41d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b41d-103">İlke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b41d-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="9b41d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b41d-104">SYNTAX</span></span>

### <span data-ttu-id="9b41d-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b41d-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b41d-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b41d-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b41d-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9b41d-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b41d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b41d-108">DESCRIPTION</span></span>
<span data-ttu-id="9b41d-109">**New-AzPolicySetDefinition** cmdlet 'i bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b41d-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="9b41d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b41d-110">EXAMPLES</span></span>

### <span data-ttu-id="9b41d-111">Örnek 1: ilke kümesi dosyası kullanarak meta verilerle ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b41d-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="9b41d-112">Bu komut, VMPolicySetDefinition adında meta veri içeren bir ilke kümesi tanımı oluşturur ve bunun kategorisinin, C:\VMPolicy.jsbelirtilen ilke tanımlarını içeren "sanal makine" olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9b41d-113">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="9b41d-114">Örnek 2: Parametreli bir ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b41d-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="9b41d-115">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren, VMPolicySetDefinition adlı parametreli bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b41d-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9b41d-116">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="9b41d-117">Örnek 3: ilke tanımı gruplarıyla ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b41d-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="9b41d-118">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarının gruplandırılması ile VMPolicySetDefinition adlı bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b41d-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9b41d-119">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="9b41d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b41d-120">PARAMETERS</span></span>

### <span data-ttu-id="9b41d-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9b41d-121">-ApiVersion</span></span>
<span data-ttu-id="9b41d-122">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9b41d-123">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9b41d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b41d-124">-DefaultProfile</span></span>
<span data-ttu-id="9b41d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9b41d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b41d-126">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9b41d-126">-Description</span></span>
<span data-ttu-id="9b41d-127">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9b41d-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="9b41d-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9b41d-128">-DisplayName</span></span>
<span data-ttu-id="9b41d-129">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="9b41d-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="9b41d-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="9b41d-130">-GroupDefinition</span></span>
<span data-ttu-id="9b41d-131">Yeni ilke kümesi tanımının ilke tanımı grupları.</span><span class="sxs-lookup"><span data-stu-id="9b41d-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="9b41d-132">Bu, grupları içeren bir dosyanın yolu veya JSON dizesi olarak gruplar olabilir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="9b41d-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9b41d-133">-ManagementGroupName</span></span>
<span data-ttu-id="9b41d-134">Yeni ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9b41d-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="9b41d-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9b41d-135">-Metadata</span></span>
<span data-ttu-id="9b41d-136">İlke kümesi tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="9b41d-136">The metadata for policy set definition.</span></span> <span data-ttu-id="9b41d-137">Bu, meta verileri içeren bir dosya adının yolu veya JSON dizesi olarak meta veri olabilir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="9b41d-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b41d-138">-Name</span></span>
<span data-ttu-id="9b41d-139">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="9b41d-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b41d-140">-Parametre</span><span class="sxs-lookup"><span data-stu-id="9b41d-140">-Parameter</span></span>
<span data-ttu-id="9b41d-141">İlke kümesi tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="9b41d-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="9b41d-142">Bu, Parameters bildirimini içeren bir dosya adına veya JSON dizesi olarak Parameters bildirimine yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="9b41d-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9b41d-143">-PolicyDefinition</span></span>
<span data-ttu-id="9b41d-144">İlke tanımları.</span><span class="sxs-lookup"><span data-stu-id="9b41d-144">The policy definitions.</span></span> <span data-ttu-id="9b41d-145">Bu, ilke tanımlarını içeren bir dosya adına veya JSON dizesi olarak ilke tanımlarına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b41d-146">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9b41d-146">-Pre</span></span>
<span data-ttu-id="9b41d-147">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9b41d-148">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9b41d-148">-SubscriptionId</span></span>
<span data-ttu-id="9b41d-149">Yeni ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9b41d-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="9b41d-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b41d-150">-Confirm</span></span>
<span data-ttu-id="9b41d-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b41d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b41d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b41d-152">-WhatIf</span></span>
<span data-ttu-id="9b41d-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b41d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b41d-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b41d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b41d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b41d-155">CommonParameters</span></span>
<span data-ttu-id="9b41d-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b41d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b41d-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b41d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b41d-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b41d-158">INPUTS</span></span>

### <span data-ttu-id="9b41d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9b41d-159">System.String</span></span>

### <span data-ttu-id="9b41d-160">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b41d-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9b41d-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b41d-161">OUTPUTS</span></span>

### <span data-ttu-id="9b41d-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9b41d-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9b41d-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b41d-163">NOTES</span></span>

## <span data-ttu-id="9b41d-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b41d-164">RELATED LINKS</span></span>
