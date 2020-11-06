---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 44cf09bdbf3f7be5a30a1b48831e975b3f42e693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572625"
---
# <span data-ttu-id="42605-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="42605-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="42605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42605-102">SYNOPSIS</span></span>
<span data-ttu-id="42605-103">İlke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42605-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42605-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42605-104">SYNTAX</span></span>

### <span data-ttu-id="42605-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42605-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42605-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42605-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42605-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="42605-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42605-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="42605-108">DESCRIPTION</span></span>
<span data-ttu-id="42605-109">**New-AzureRmPolicySetDefinition** cmdlet 'i bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42605-109">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="42605-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42605-110">EXAMPLES</span></span>

### <span data-ttu-id="42605-111">Örnek 1: ilke kümesi dosyası kullanarak ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="42605-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="42605-112">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren VMPolicyDefinition adlı bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42605-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="42605-113">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="42605-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="42605-114">Örnek 2: Parametreli bir ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="42605-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="42605-115">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren, VMPolicyDefinition adlı parametreli bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42605-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="42605-116">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="42605-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="42605-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42605-117">PARAMETERS</span></span>

### <span data-ttu-id="42605-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="42605-118">-ApiVersion</span></span>
<span data-ttu-id="42605-119">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="42605-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="42605-120">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42605-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="42605-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42605-121">-DefaultProfile</span></span>
<span data-ttu-id="42605-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42605-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42605-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="42605-123">-Description</span></span>
<span data-ttu-id="42605-124">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="42605-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="42605-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="42605-125">-DisplayName</span></span>
<span data-ttu-id="42605-126">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="42605-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="42605-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="42605-127">-ManagementGroupName</span></span>
<span data-ttu-id="42605-128">Yeni ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="42605-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="42605-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="42605-129">-Metadata</span></span>
<span data-ttu-id="42605-130">İlke kümesi tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="42605-130">The metadata for policy set definition.</span></span> <span data-ttu-id="42605-131">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="42605-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="42605-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="42605-132">-Name</span></span>
<span data-ttu-id="42605-133">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="42605-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="42605-134">-Parametre</span><span class="sxs-lookup"><span data-stu-id="42605-134">-Parameter</span></span>
<span data-ttu-id="42605-135">İlke kümesi tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="42605-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="42605-136">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="42605-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="42605-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42605-137">-PolicyDefinition</span></span>
<span data-ttu-id="42605-138">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="42605-138">The policy set definition.</span></span> <span data-ttu-id="42605-139">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="42605-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="42605-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="42605-140">-Pre</span></span>
<span data-ttu-id="42605-141">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42605-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="42605-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="42605-142">-SubscriptionId</span></span>
<span data-ttu-id="42605-143">Yeni ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="42605-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="42605-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="42605-144">-Confirm</span></span>
<span data-ttu-id="42605-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42605-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42605-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42605-146">-WhatIf</span></span>
<span data-ttu-id="42605-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42605-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42605-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42605-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42605-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42605-149">CommonParameters</span></span>
<span data-ttu-id="42605-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42605-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42605-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42605-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42605-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42605-152">INPUTS</span></span>

### <span data-ttu-id="42605-153">System. String</span><span class="sxs-lookup"><span data-stu-id="42605-153">System.String</span></span>

### <span data-ttu-id="42605-154">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="42605-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="42605-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42605-155">OUTPUTS</span></span>

### <span data-ttu-id="42605-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="42605-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="42605-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42605-157">NOTES</span></span>

## <span data-ttu-id="42605-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42605-158">RELATED LINKS</span></span>
