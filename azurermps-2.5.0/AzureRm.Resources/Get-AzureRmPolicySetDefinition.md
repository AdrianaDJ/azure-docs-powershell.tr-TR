---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: b7dd9dd74417fdf1cc0a4f654eb9b11311986229
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939485"
---
# <span data-ttu-id="e8cc9-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e8cc9-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e8cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cc9-103">İlke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8cc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8cc9-104">SYNTAX</span></span>

### <span data-ttu-id="e8cc9-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8cc9-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cc9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cc9-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cc9-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e8cc9-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cc9-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="e8cc9-108">IdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cc9-109">Buılfilterparameterset</span><span class="sxs-lookup"><span data-stu-id="e8cc9-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8cc9-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cc9-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8cc9-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8cc9-111">DESCRIPTION</span></span>
<span data-ttu-id="e8cc9-112">**Get-AzureRmPolicySetDefinition** cmdlet 'i, ilke kümesi tanımlarının veya ad veya kimlikle tanımlanan belirli bir ilke kümesi tanımı koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-112">The **Get-AzureRmPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="e8cc9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8cc9-113">EXAMPLES</span></span>

### <span data-ttu-id="e8cc9-114">Örnek 1: tüm ilke kümesi tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="e8cc9-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="e8cc9-115">Bu komut, tüm ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="e8cc9-116">Örnek 2: geçerli abonelikten ilke kümesi tanımını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="e8cc9-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="e8cc9-117">Bu komut, VMPolicySetDefinition adındaki ilke kümesi tanımını geçerli varsayılan abonelikten alır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="e8cc9-118">Örnek 3: ad ile abonelikten ilke kümesi tanımını alma</span><span class="sxs-lookup"><span data-stu-id="e8cc9-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="e8cc9-119">Bu komut, VMPolicySetDefinition adlı aboneliğin KIMLIĞI 3bf44b72-c631-427A-b8c8-53e2595398ca olan abonelikten alır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="e8cc9-120">Örnek 4: tüm özel ilke kümesi tanımlarını yönetim grubundan alma</span><span class="sxs-lookup"><span data-stu-id="e8cc9-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="e8cc9-121">Bu komut, Dept42 adlı yönetim grubundan tüm özel ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="e8cc9-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8cc9-122">PARAMETERS</span></span>

### <span data-ttu-id="e8cc9-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e8cc9-123">-ApiVersion</span></span>
<span data-ttu-id="e8cc9-124">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e8cc9-125">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e8cc9-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="e8cc9-126">-Builtin</span></span>
<span data-ttu-id="e8cc9-127">Yalnızca yerleşik ilke kümesi tanımlarının sonuç listesini kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="e8cc9-128">-Özel</span><span class="sxs-lookup"><span data-stu-id="e8cc9-128">-Custom</span></span>
<span data-ttu-id="e8cc9-129">Sonuçların listesini yalnızca özel ilke kümesi tanımlarına göre sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="e8cc9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cc9-130">-DefaultProfile</span></span>
<span data-ttu-id="e8cc9-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e8cc9-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8cc9-132">-ID</span><span class="sxs-lookup"><span data-stu-id="e8cc9-132">-Id</span></span>
<span data-ttu-id="e8cc9-133">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="e8cc9-134">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="e8cc9-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e8cc9-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cc9-135">-ManagementGroupName</span></span>
<span data-ttu-id="e8cc9-136">Alınacak ilke kümesi tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="e8cc9-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8cc9-137">-Name</span></span>
<span data-ttu-id="e8cc9-138">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="e8cc9-139">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e8cc9-139">-Pre</span></span>
<span data-ttu-id="e8cc9-140">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e8cc9-141">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e8cc9-141">-SubscriptionId</span></span>
<span data-ttu-id="e8cc9-142">Alınacak ilke kümesi tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="e8cc9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cc9-143">CommonParameters</span></span>
<span data-ttu-id="e8cc9-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8cc9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cc9-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8cc9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cc9-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8cc9-146">INPUTS</span></span>

### <span data-ttu-id="e8cc9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e8cc9-147">System.String</span></span>

### <span data-ttu-id="e8cc9-148">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e8cc9-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e8cc9-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8cc9-149">OUTPUTS</span></span>

### <span data-ttu-id="e8cc9-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e8cc9-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e8cc9-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8cc9-151">NOTES</span></span>

## <span data-ttu-id="e8cc9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8cc9-152">RELATED LINKS</span></span>
