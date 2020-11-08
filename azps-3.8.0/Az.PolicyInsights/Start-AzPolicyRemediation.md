---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098447"
---
# <span data-ttu-id="0b2b5-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0b2b5-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="0b2b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2b5-103">İlke ataması için ilke düzeltmesi oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="0b2b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b2b5-104">SYNTAX</span></span>

### <span data-ttu-id="0b2b5-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b2b5-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2b5-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0b2b5-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b2b5-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2b5-108">**Start-Azpolicydüzeltme** cmdlet 'i belirli bir ilke ataması için bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="0b2b5-109">Düzeltmenin kapsamının veya altındaki uyumlu olmayan tüm kaynaklar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="0b2b5-110">Düzeltme yalnızca ' deployIfNotExists ' efektine sahip ilkelerde desteklenir.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="0b2b5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b2b5-111">EXAMPLES</span></span>

### <span data-ttu-id="0b2b5-112">Örnek 1: abonelik kapsamında düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="0b2b5-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="0b2b5-113">Bu komut, verilen ilke ataması için ' Aboneliğimin ' aboneliğindeki yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="0b2b5-114">Örnek 2: isteğe bağlı filtrelerle yönetim grubu kapsamında düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="0b2b5-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="0b2b5-115">Bu komut, verilen ilke ataması için ' MG1 ' yönetim grubunda yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="0b2b5-116">Yalnızca ' westus ' veya ' eastus ' konumlarındaki kaynaklar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="0b2b5-117">Örnek 3: ilke kümesi tanımı ataması için kaynak grup kapsamında düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="0b2b5-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="0b2b5-118">Bu komut, verilen ilke ataması için ' myRG ' kaynak grubunda yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="0b2b5-119">İlke ataması bir ilke kümesi tanımı atar (bir Initiative olarak da bilinir).</span><span class="sxs-lookup"><span data-stu-id="0b2b5-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="0b2b5-120">İlke tanımı başvuru KIMLIĞI, Initiative 'deki hangi ilkenin düzeltilmeli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="0b2b5-121">Örnek 4: düzeltme başlatma ve arka planda tamamlamasını bekleme</span><span class="sxs-lookup"><span data-stu-id="0b2b5-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="0b2b5-122">Bu komut, verilen ilke ataması için ' Aboneliğimin ' aboneliğindeki yeni bir ilke düzeltmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="0b2b5-123">Son düzeltme durumunu döndürmeden düzeltmenin tamamlanmasını bekleyecek.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="0b2b5-124">Örnek 5: düzeltmeden önce uyumlu olmayan kaynakları keşfeden düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="0b2b5-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="0b2b5-125">Bu komut, verilen ilke ataması için ' Aboneliğimin ' aboneliğindeki yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="0b2b5-126">Abonelikteki kaynakların uyumluluk durumu, ilke atamasında ve uyumlu olmayan kaynaklar için yeniden değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="0b2b5-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b2b5-127">PARAMETERS</span></span>

### <span data-ttu-id="0b2b5-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b2b5-128">-AsJob</span></span>
<span data-ttu-id="0b2b5-129">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0b2b5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2b5-130">-DefaultProfile</span></span>
<span data-ttu-id="0b2b5-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2b5-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="0b2b5-132">-LocationFilter</span></span>
<span data-ttu-id="0b2b5-133">Düzeltmeye dahil edilmesi gereken kaynak konumları.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="0b2b5-134">Bu konumlarda bulunmayan kaynaklar düzeltilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b5-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2b5-135">-ManagementGroupName</span></span>
<span data-ttu-id="0b2b5-136">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-136">Management group ID.</span></span>

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

### <span data-ttu-id="0b2b5-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b2b5-137">-Name</span></span>
<span data-ttu-id="0b2b5-138">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-138">Resource name.</span></span>

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

### <span data-ttu-id="0b2b5-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="0b2b5-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="0b2b5-140">İlke atama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-140">Policy assignment ID.</span></span>
<span data-ttu-id="0b2b5-141">Yani.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-141">E.g.</span></span>
<span data-ttu-id="0b2b5-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="0b2b5-143">-Policydefinitionreferenceıd</span><span class="sxs-lookup"><span data-stu-id="0b2b5-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="0b2b5-144">Düzeltilen tek tanımın ilke tanımı başvuru KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="0b2b5-145">İlke ataması bir ilke kümesi tanımı atarsa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="0b2b5-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="0b2b5-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="0b2b5-147">Düzeltme görevinin, başlatılması gereken kaynakları nasıl keşfedeceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="0b2b5-148">Yönetim grubu kapsamlarını düzeltme işlemi yapılırken Ateuyumluluğu yeniden değerlendirilmiyor.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2b5-149">-ResourceGroupName</span></span>
<span data-ttu-id="0b2b5-150">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-150">Resource group name.</span></span>

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

### <span data-ttu-id="0b2b5-151">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b2b5-151">-ResourceId</span></span>
<span data-ttu-id="0b2b5-152">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-152">Resource ID.</span></span>

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

### <span data-ttu-id="0b2b5-153">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0b2b5-153">-Scope</span></span>
<span data-ttu-id="0b2b5-154">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-154">Scope of the resource.</span></span>
<span data-ttu-id="0b2b5-155">Yani.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-155">E.g.</span></span>
<span data-ttu-id="0b2b5-156">'/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="0b2b5-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b2b5-157">-Confirm</span></span>
<span data-ttu-id="0b2b5-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2b5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2b5-159">-WhatIf</span></span>
<span data-ttu-id="0b2b5-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2b5-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2b5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2b5-162">CommonParameters</span></span>
<span data-ttu-id="0b2b5-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2b5-164">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2b5-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b2b5-165">INPUTS</span></span>

### <span data-ttu-id="0b2b5-166">System. String</span><span class="sxs-lookup"><span data-stu-id="0b2b5-166">System.String</span></span>

### <span data-ttu-id="0b2b5-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="0b2b5-167">System.String[]</span></span>

## <span data-ttu-id="0b2b5-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b2b5-168">OUTPUTS</span></span>

### <span data-ttu-id="0b2b5-169">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="0b2b5-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="0b2b5-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b2b5-170">NOTES</span></span>

## <span data-ttu-id="0b2b5-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b2b5-171">RELATED LINKS</span></span>