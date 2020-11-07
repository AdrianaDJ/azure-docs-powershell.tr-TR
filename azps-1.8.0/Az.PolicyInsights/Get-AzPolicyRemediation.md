---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44f7d3331d32092636c53850b0315f34b7df7808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759828"
---
# <span data-ttu-id="0adba-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0adba-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="0adba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0adba-102">SYNOPSIS</span></span>
<span data-ttu-id="0adba-103">İlke değişikliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="0adba-103">Gets policy remediations.</span></span>

## <span data-ttu-id="0adba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0adba-104">SYNTAX</span></span>

### <span data-ttu-id="0adba-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0adba-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0adba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0adba-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0adba-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="0adba-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0adba-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="0adba-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0adba-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="0adba-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0adba-110">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0adba-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0adba-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="0adba-111">DESCRIPTION</span></span>
<span data-ttu-id="0adba-112">**Get-Azilkedüzeltme** cmdlet 'inde tüm ilke değişikliklerini veya belirli bir düzeltmeyi alır.</span><span class="sxs-lookup"><span data-stu-id="0adba-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="0adba-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0adba-113">EXAMPLES</span></span>

### <span data-ttu-id="0adba-114">Örnek 1: geçerli abonelikteki tüm ilke değişikliklerini alma</span><span class="sxs-lookup"><span data-stu-id="0adba-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="0adba-115">Bu komut, ' Aboneliğimin ' adlı bir aboneliğin veya altında oluşturulan tüm değişiklikleri alır.</span><span class="sxs-lookup"><span data-stu-id="0adba-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="0adba-116">Örnek 2: belirli bir ilke düzeltmesini ve dağıtım ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="0adba-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="0adba-117">Bu komut, ' myResourceGroup ' kaynak grubundan ' remediation1 ' adındaki düzeltmeyi alır.</span><span class="sxs-lookup"><span data-stu-id="0adba-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="0adba-118">Düzeltilen kaynakların ayrıntıları dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="0adba-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="0adba-119">Örnek 3: isteğe bağlı filtreler içeren bir yönetim grubundaki 10 ilke ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="0adba-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="0adba-120">Bu komut, ' MG1 ' adlı bir yönetim grubundan en fazla 10 poliçe ayarı alır.</span><span class="sxs-lookup"><span data-stu-id="0adba-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="0adba-121">Yalnızca verilen ilke atamasının ilke değişiklikleri alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="0adba-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="0adba-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0adba-122">PARAMETERS</span></span>

### <span data-ttu-id="0adba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0adba-123">-DefaultProfile</span></span>
<span data-ttu-id="0adba-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0adba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0adba-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="0adba-125">-Filter</span></span>
<span data-ttu-id="0adba-126">OData gösterimini kullanan filtre ifadesi.</span><span class="sxs-lookup"><span data-stu-id="0adba-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="0adba-127">-Includedetail</span><span class="sxs-lookup"><span data-stu-id="0adba-127">-IncludeDetail</span></span>
<span data-ttu-id="0adba-128">Düzeltme tarafından oluşturulan dağıtımların ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0adba-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="0adba-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0adba-129">-ManagementGroupName</span></span>
<span data-ttu-id="0adba-130">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0adba-130">Management group ID.</span></span>

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

### <span data-ttu-id="0adba-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="0adba-131">-Name</span></span>
<span data-ttu-id="0adba-132">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0adba-132">Resource name.</span></span>

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

### <span data-ttu-id="0adba-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0adba-133">-ResourceGroupName</span></span>
<span data-ttu-id="0adba-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0adba-134">Resource group name.</span></span>

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

### <span data-ttu-id="0adba-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0adba-135">-ResourceId</span></span>
<span data-ttu-id="0adba-136">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0adba-136">Resource ID.</span></span>

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

### <span data-ttu-id="0adba-137">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0adba-137">-Scope</span></span>
<span data-ttu-id="0adba-138">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="0adba-138">Scope of the resource.</span></span> <span data-ttu-id="0adba-139">Örneğin, '/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="0adba-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="0adba-140">-Üst</span><span class="sxs-lookup"><span data-stu-id="0adba-140">-Top</span></span>
<span data-ttu-id="0adba-141">Döndürülecek en fazla kayıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="0adba-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="0adba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0adba-142">CommonParameters</span></span>
<span data-ttu-id="0adba-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0adba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0adba-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0adba-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0adba-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0adba-145">INPUTS</span></span>

### <span data-ttu-id="0adba-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0adba-146">System.String</span></span>

## <span data-ttu-id="0adba-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0adba-147">OUTPUTS</span></span>

### <span data-ttu-id="0adba-148">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="0adba-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="0adba-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0adba-149">NOTES</span></span>

## <span data-ttu-id="0adba-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0adba-150">RELATED LINKS</span></span>