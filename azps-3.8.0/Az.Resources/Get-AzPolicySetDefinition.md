---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098097"
---
# <span data-ttu-id="a6a7e-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a6a7e-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="a6a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a7e-103">İlke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="a6a7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6a7e-104">SYNTAX</span></span>

### <span data-ttu-id="a6a7e-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6a7e-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a7e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a7e-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a7e-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a6a7e-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a7e-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="a6a7e-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6a7e-109">Buılfilterparameterset</span><span class="sxs-lookup"><span data-stu-id="a6a7e-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a7e-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a7e-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a7e-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6a7e-111">DESCRIPTION</span></span>
<span data-ttu-id="a6a7e-112">**Get-AzPolicySetDefinition** cmdlet 'i, ilke kümesi tanımlarının veya ad veya kimlikle tanımlanan belirli bir ilke kümesi tanımı koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="a6a7e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6a7e-113">EXAMPLES</span></span>

### <span data-ttu-id="a6a7e-114">Örnek 1: tüm ilke kümesi tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="a6a7e-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="a6a7e-115">Bu komut, tüm ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="a6a7e-116">Örnek 2: geçerli abonelikten ilke kümesi tanımını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="a6a7e-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="a6a7e-117">Bu komut, VMPolicySetDefinition adındaki ilke kümesi tanımını geçerli varsayılan abonelikten alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="a6a7e-118">Örnek 3: ad ile abonelikten ilke kümesi tanımını alma</span><span class="sxs-lookup"><span data-stu-id="a6a7e-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="a6a7e-119">Bu komut, VMPolicySetDefinition adlı aboneliğin KIMLIĞI 3bf44b72-c631-427A-b8c8-53e2595398ca olan abonelikten alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="a6a7e-120">Örnek 4: tüm özel ilke kümesi tanımlarını yönetim grubundan alma</span><span class="sxs-lookup"><span data-stu-id="a6a7e-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="a6a7e-121">Bu komut, Dept42 adlı yönetim grubundan tüm özel ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="a6a7e-122">Örnek 5: verilen kategoriden ilke kümesi tanımları alma</span><span class="sxs-lookup"><span data-stu-id="a6a7e-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="a6a7e-123">Bu komut, "sanal makine" kategorisindeki tüm ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="a6a7e-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6a7e-124">PARAMETERS</span></span>

### <span data-ttu-id="a6a7e-125">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a6a7e-125">-ApiVersion</span></span>
<span data-ttu-id="a6a7e-126">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a6a7e-127">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a6a7e-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="a6a7e-128">-Builtin</span></span>
<span data-ttu-id="a6a7e-129">Yalnızca yerleşik ilke kümesi tanımlarının sonuç listesini kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a7e-130">-Özel</span><span class="sxs-lookup"><span data-stu-id="a6a7e-130">-Custom</span></span>
<span data-ttu-id="a6a7e-131">Sonuçların listesini yalnızca özel ilke kümesi tanımlarına göre sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a7e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a7e-132">-DefaultProfile</span></span>
<span data-ttu-id="a6a7e-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a6a7e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6a7e-134">-ID</span><span class="sxs-lookup"><span data-stu-id="a6a7e-134">-Id</span></span>
<span data-ttu-id="a6a7e-135">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="a6a7e-136">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="a6a7e-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a6a7e-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a7e-137">-ManagementGroupName</span></span>
<span data-ttu-id="a6a7e-138">Alınacak ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a7e-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6a7e-139">-Name</span></span>
<span data-ttu-id="a6a7e-140">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a7e-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a6a7e-141">-Pre</span></span>
<span data-ttu-id="a6a7e-142">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a6a7e-143">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a6a7e-143">-SubscriptionId</span></span>
<span data-ttu-id="a6a7e-144">Alınacak ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a7e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a7e-145">CommonParameters</span></span>
<span data-ttu-id="a6a7e-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a7e-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a6a7e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a7e-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6a7e-148">INPUTS</span></span>

### <span data-ttu-id="a6a7e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a6a7e-149">System.String</span></span>

### <span data-ttu-id="a6a7e-150">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6a7e-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a6a7e-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6a7e-151">OUTPUTS</span></span>

### <span data-ttu-id="a6a7e-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a6a7e-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a6a7e-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6a7e-153">NOTES</span></span>

## <span data-ttu-id="a6a7e-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6a7e-154">RELATED LINKS</span></span>
