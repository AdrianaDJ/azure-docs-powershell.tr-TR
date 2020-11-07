---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 838fe6f4ed7ff1e69a6bdf99a8816f00fc0ab019
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933342"
---
# <span data-ttu-id="31ef4-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="31ef4-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="31ef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="31ef4-103">İlke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31ef4-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="31ef4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31ef4-104">SYNTAX</span></span>

### <span data-ttu-id="31ef4-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31ef4-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ef4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ef4-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ef4-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="31ef4-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ef4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="31ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="31ef4-109">**New-AzPolicySetDefinition** cmdlet 'i bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31ef4-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="31ef4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31ef4-110">EXAMPLES</span></span>

### <span data-ttu-id="31ef4-111">Örnek 1: ilke kümesi dosyası kullanarak meta verilerle ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="31ef4-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="31ef4-112">Bu komut, VMPolicySetDefinition adında meta veri içeren bir ilke kümesi tanımı oluşturur ve bunun kategorisinin, C:\VMPolicy.jsbelirtilen ilke tanımlarını içeren "sanal makine" olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="31ef4-113">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="31ef4-114">Örnek 2: Parametreli bir ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="31ef4-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="31ef4-115">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren, VMPolicySetDefinition adlı parametreli bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31ef4-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="31ef4-116">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="31ef4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31ef4-117">PARAMETERS</span></span>

### <span data-ttu-id="31ef4-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="31ef4-118">-ApiVersion</span></span>
<span data-ttu-id="31ef4-119">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="31ef4-120">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="31ef4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ef4-121">-DefaultProfile</span></span>
<span data-ttu-id="31ef4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="31ef4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31ef4-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="31ef4-123">-Description</span></span>
<span data-ttu-id="31ef4-124">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="31ef4-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="31ef4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="31ef4-125">-DisplayName</span></span>
<span data-ttu-id="31ef4-126">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="31ef4-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="31ef4-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="31ef4-127">-ManagementGroupName</span></span>
<span data-ttu-id="31ef4-128">Yeni ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="31ef4-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="31ef4-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="31ef4-129">-Metadata</span></span>
<span data-ttu-id="31ef4-130">İlke kümesi tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="31ef4-130">The metadata for policy set definition.</span></span> <span data-ttu-id="31ef4-131">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="31ef4-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="31ef4-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="31ef4-132">-Name</span></span>
<span data-ttu-id="31ef4-133">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="31ef4-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="31ef4-134">-Parametre</span><span class="sxs-lookup"><span data-stu-id="31ef4-134">-Parameter</span></span>
<span data-ttu-id="31ef4-135">İlke kümesi tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="31ef4-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="31ef4-136">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="31ef4-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31ef4-137">-PolicyDefinition</span></span>
<span data-ttu-id="31ef4-138">İlke tanımları.</span><span class="sxs-lookup"><span data-stu-id="31ef4-138">The policy definitions.</span></span> <span data-ttu-id="31ef4-139">Bu, ilke tanımlarını içeren bir dosya adına veya dizi olarak ilke tanımlarına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-139">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="31ef4-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="31ef4-140">-Pre</span></span>
<span data-ttu-id="31ef4-141">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="31ef4-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="31ef4-142">-SubscriptionId</span></span>
<span data-ttu-id="31ef4-143">Yeni ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="31ef4-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="31ef4-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="31ef4-144">-Confirm</span></span>
<span data-ttu-id="31ef4-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31ef4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ef4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ef4-146">-WhatIf</span></span>
<span data-ttu-id="31ef4-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31ef4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31ef4-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31ef4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ef4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ef4-149">CommonParameters</span></span>
<span data-ttu-id="31ef4-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31ef4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ef4-151">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="31ef4-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ef4-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31ef4-152">INPUTS</span></span>

### <span data-ttu-id="31ef4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="31ef4-153">System.String</span></span>

### <span data-ttu-id="31ef4-154">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="31ef4-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="31ef4-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31ef4-155">OUTPUTS</span></span>

### <span data-ttu-id="31ef4-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="31ef4-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="31ef4-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31ef4-157">NOTES</span></span>

## <span data-ttu-id="31ef4-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31ef4-158">RELATED LINKS</span></span>
