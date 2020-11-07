---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: c5de339929e44433efdee64de0257c62845c5b26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936391"
---
# <span data-ttu-id="9fe9e-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9fe9e-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="9fe9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe9e-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe9e-103">İlke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="9fe9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fe9e-104">SYNTAX</span></span>

### <span data-ttu-id="9fe9e-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fe9e-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe9e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe9e-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe9e-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9fe9e-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fe9e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fe9e-108">DESCRIPTION</span></span>
<span data-ttu-id="9fe9e-109">**New-AzPolicySetDefinition** cmdlet 'i bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="9fe9e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fe9e-110">EXAMPLES</span></span>

### <span data-ttu-id="9fe9e-111">Örnek 1: ilke kümesi dosyası kullanarak ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9fe9e-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="9fe9e-112">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren VMPolicyDefinition adlı bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9fe9e-113">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="9fe9e-114">Örnek 2: Parametreli bir ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9fe9e-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="9fe9e-115">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren, VMPolicyDefinition adlı parametreli bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9fe9e-116">VMPolicy.jsörnek içeriği yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="9fe9e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fe9e-117">PARAMETERS</span></span>

### <span data-ttu-id="9fe9e-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9fe9e-118">-ApiVersion</span></span>
<span data-ttu-id="9fe9e-119">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9fe9e-120">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9fe9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe9e-121">-DefaultProfile</span></span>
<span data-ttu-id="9fe9e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9fe9e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9e-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9fe9e-123">-Description</span></span>
<span data-ttu-id="9fe9e-124">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="9fe9e-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9fe9e-125">-DisplayName</span></span>
<span data-ttu-id="9fe9e-126">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="9fe9e-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe9e-127">-ManagementGroupName</span></span>
<span data-ttu-id="9fe9e-128">Yeni ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="9fe9e-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9fe9e-129">-Metadata</span></span>
<span data-ttu-id="9fe9e-130">İlke kümesi tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-130">The metadata for policy set definition.</span></span> <span data-ttu-id="9fe9e-131">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="9fe9e-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="9fe9e-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fe9e-132">-Name</span></span>
<span data-ttu-id="9fe9e-133">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="9fe9e-134">-Parametre</span><span class="sxs-lookup"><span data-stu-id="9fe9e-134">-Parameter</span></span>
<span data-ttu-id="9fe9e-135">İlke kümesi tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="9fe9e-136">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="9fe9e-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9fe9e-137">-PolicyDefinition</span></span>
<span data-ttu-id="9fe9e-138">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-138">The policy set definition.</span></span> <span data-ttu-id="9fe9e-139">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="9fe9e-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9fe9e-140">-Pre</span></span>
<span data-ttu-id="9fe9e-141">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9fe9e-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9fe9e-142">-SubscriptionId</span></span>
<span data-ttu-id="9fe9e-143">Yeni ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="9fe9e-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fe9e-144">-Confirm</span></span>
<span data-ttu-id="9fe9e-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe9e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe9e-146">-WhatIf</span></span>
<span data-ttu-id="9fe9e-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fe9e-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe9e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe9e-149">CommonParameters</span></span>
<span data-ttu-id="9fe9e-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fe9e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe9e-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe9e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe9e-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fe9e-152">INPUTS</span></span>

### <span data-ttu-id="9fe9e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe9e-153">System.String</span></span>

### <span data-ttu-id="9fe9e-154">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9fe9e-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9fe9e-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fe9e-155">OUTPUTS</span></span>

### <span data-ttu-id="9fe9e-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9fe9e-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9fe9e-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fe9e-157">NOTES</span></span>

## <span data-ttu-id="9fe9e-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fe9e-158">RELATED LINKS</span></span>
