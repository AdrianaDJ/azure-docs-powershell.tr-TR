---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
ms.openlocfilehash: e69ad25800dbf6aada7111a1093b4c878f3c0f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593196"
---
# <span data-ttu-id="4cf65-101">Get-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4cf65-101">Get-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="4cf65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf65-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf65-103">İlke değişikliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4cf65-103">Gets policy remediations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cf65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cf65-104">SYNTAX</span></span>

### <span data-ttu-id="4cf65-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4cf65-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cf65-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4cf65-106">ByName</span></span>
```
Get-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cf65-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="4cf65-107">GenericScope</span></span>
```
Get-AzureRmPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf65-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="4cf65-108">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf65-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="4cf65-109">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf65-110">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4cf65-110">ByResourceId</span></span>
```
Get-AzureRmPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf65-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cf65-111">DESCRIPTION</span></span>
<span data-ttu-id="4cf65-112">**Get-AzureRmPolicyRemediation** cmdlet 'i, bir kapsam veya belirli bir düzeltmenin tüm ilke değişikliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4cf65-112">The **Get-AzureRmPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="4cf65-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cf65-113">EXAMPLES</span></span>

### <span data-ttu-id="4cf65-114">Örnek 1: geçerli abonelikteki tüm ilke değişikliklerini alma</span><span class="sxs-lookup"><span data-stu-id="4cf65-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Get-AzureRmPolicyRemediation
```

<span data-ttu-id="4cf65-115">Bu komut, ' Aboneliğimin ' adlı bir aboneliğin veya altında oluşturulan tüm değişiklikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4cf65-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="4cf65-116">Örnek 2: belirli bir ilke düzeltmesini ve dağıtım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="4cf65-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="4cf65-117">Bu komut, ' myResourceGroup ' kaynak grubundan ' remediation1 ' adındaki düzeltmeyi alır.</span><span class="sxs-lookup"><span data-stu-id="4cf65-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="4cf65-118">Düzeltilen kaynakların ayrıntıları dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="4cf65-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="4cf65-119">Örnek 3: isteğe bağlı filtreler içeren bir yönetim grubundaki 10 ilke ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="4cf65-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="4cf65-120">Bu komut, ' MG1 ' adlı bir yönetim grubundan en fazla 10 poliçe ayarı alır.</span><span class="sxs-lookup"><span data-stu-id="4cf65-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="4cf65-121">Yalnızca verilen ilke atamasının ilke değişiklikleri alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="4cf65-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="4cf65-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cf65-122">PARAMETERS</span></span>

### <span data-ttu-id="4cf65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf65-123">-DefaultProfile</span></span>
<span data-ttu-id="4cf65-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cf65-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf65-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="4cf65-125">-Filter</span></span>
<span data-ttu-id="4cf65-126">OData gösterimini kullanan filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="4cf65-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-127">-Includedetail</span><span class="sxs-lookup"><span data-stu-id="4cf65-127">-IncludeDetail</span></span>
<span data-ttu-id="4cf65-128">Düzeltme tarafından oluşturulan dağıtımların ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4cf65-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf65-129">-ManagementGroupName</span></span>
<span data-ttu-id="4cf65-130">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4cf65-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cf65-131">-Name</span></span>
<span data-ttu-id="4cf65-132">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4cf65-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf65-133">-ResourceGroupName</span></span>
<span data-ttu-id="4cf65-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4cf65-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4cf65-135">-ResourceId</span></span>
<span data-ttu-id="4cf65-136">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4cf65-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-137">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="4cf65-137">-Scope</span></span>
<span data-ttu-id="4cf65-138">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="4cf65-138">Scope of the resource.</span></span> <span data-ttu-id="4cf65-139">Örneğin, '/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="4cf65-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-140">-Üst</span><span class="sxs-lookup"><span data-stu-id="4cf65-140">-Top</span></span>
<span data-ttu-id="4cf65-141">Döndürülecek en fazla kayıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="4cf65-141">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf65-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf65-142">CommonParameters</span></span>
<span data-ttu-id="4cf65-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cf65-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf65-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf65-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf65-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cf65-145">INPUTS</span></span>

### <span data-ttu-id="4cf65-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4cf65-146">System.String</span></span>

## <span data-ttu-id="4cf65-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cf65-147">OUTPUTS</span></span>

### <span data-ttu-id="4cf65-148">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="4cf65-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="4cf65-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cf65-149">NOTES</span></span>

## <span data-ttu-id="4cf65-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cf65-150">RELATED LINKS</span></span>
