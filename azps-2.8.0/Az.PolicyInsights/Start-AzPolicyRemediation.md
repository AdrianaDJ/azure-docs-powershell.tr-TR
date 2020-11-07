---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: df7b0803952a7a972d2c68ef2d8e7ec61d42c5e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932820"
---
# <span data-ttu-id="40f90-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="40f90-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="40f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f90-102">SYNOPSIS</span></span>
<span data-ttu-id="40f90-103">İlke ataması için ilke düzeltmesi oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="40f90-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="40f90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40f90-104">SYNTAX</span></span>

### <span data-ttu-id="40f90-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40f90-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40f90-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="40f90-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40f90-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="40f90-107">DESCRIPTION</span></span>
<span data-ttu-id="40f90-108">**Start-Azpolicydüzeltme** cmdlet 'i belirli bir ilke ataması için bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40f90-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="40f90-109">Düzeltmenin kapsamının veya altındaki uyumlu olmayan tüm kaynaklar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="40f90-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="40f90-110">Düzeltme yalnızca ' deployIfNotExists ' efektine sahip ilkelerde desteklenir.</span><span class="sxs-lookup"><span data-stu-id="40f90-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="40f90-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40f90-111">EXAMPLES</span></span>

### <span data-ttu-id="40f90-112">Örnek 1: abonelik kapsamında düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="40f90-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="40f90-113">Bu komut, verilen ilke ataması için ' Aboneliğimin ' aboneliğindeki yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40f90-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="40f90-114">Örnek 2: isteğe bağlı filtrelerle yönetim grubu kapsamında düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="40f90-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="40f90-115">Bu komut, verilen ilke ataması için ' MG1 ' yönetim grubunda yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40f90-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="40f90-116">Yalnızca ' westus ' veya ' eastus ' konumlarındaki kaynaklar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="40f90-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="40f90-117">Örnek 3: ilke kümesi tanımı ataması için kaynak grup kapsamında düzeltme başlatma</span><span class="sxs-lookup"><span data-stu-id="40f90-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="40f90-118">Bu komut, verilen ilke ataması için ' myRG ' kaynak grubunda yeni bir ilke düzeltmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40f90-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="40f90-119">İlke ataması bir ilke kümesi tanımı atar (bir Initiative olarak da bilinir).</span><span class="sxs-lookup"><span data-stu-id="40f90-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="40f90-120">İlke tanımı başvuru KIMLIĞI, Initiative 'deki hangi ilkenin düzeltilmeli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="40f90-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="40f90-121">Örnek 4: düzeltme başlatma ve arka planda tamamlamasını bekleme</span><span class="sxs-lookup"><span data-stu-id="40f90-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="40f90-122">Bu komut, verilen ilke ataması için ' Aboneliğimin ' aboneliğindeki yeni bir ilke düzeltmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="40f90-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="40f90-123">Son düzeltme durumunu döndürmeden düzeltmenin tamamlanmasını bekleyecek.</span><span class="sxs-lookup"><span data-stu-id="40f90-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="40f90-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40f90-124">PARAMETERS</span></span>

### <span data-ttu-id="40f90-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="40f90-125">-AsJob</span></span>
<span data-ttu-id="40f90-126">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="40f90-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="40f90-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f90-127">-DefaultProfile</span></span>
<span data-ttu-id="40f90-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40f90-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f90-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="40f90-129">-LocationFilter</span></span>
<span data-ttu-id="40f90-130">Düzeltmeye dahil edilmesi gereken kaynak konumları.</span><span class="sxs-lookup"><span data-stu-id="40f90-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="40f90-131">Bu konumlarda bulunmayan kaynaklar düzeltilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="40f90-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="40f90-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="40f90-132">-ManagementGroupName</span></span>
<span data-ttu-id="40f90-133">Yönetim grubu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="40f90-133">Management group ID.</span></span>

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

### <span data-ttu-id="40f90-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="40f90-134">-Name</span></span>
<span data-ttu-id="40f90-135">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="40f90-135">Resource name.</span></span>

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

### <span data-ttu-id="40f90-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="40f90-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="40f90-137">İlke atama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="40f90-137">Policy assignment ID.</span></span>
<span data-ttu-id="40f90-138">Yani.</span><span class="sxs-lookup"><span data-stu-id="40f90-138">E.g.</span></span>
<span data-ttu-id="40f90-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="40f90-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="40f90-140">-Policydefinitionreferenceıd</span><span class="sxs-lookup"><span data-stu-id="40f90-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="40f90-141">Düzeltilen tek tanımın ilke tanımı başvuru KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="40f90-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="40f90-142">İlke ataması bir ilke kümesi tanımı atarsa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="40f90-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="40f90-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f90-143">-ResourceGroupName</span></span>
<span data-ttu-id="40f90-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="40f90-144">Resource group name.</span></span>

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

### <span data-ttu-id="40f90-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="40f90-145">-ResourceId</span></span>
<span data-ttu-id="40f90-146">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="40f90-146">Resource ID.</span></span>

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

### <span data-ttu-id="40f90-147">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="40f90-147">-Scope</span></span>
<span data-ttu-id="40f90-148">Kaynağın kapsamı.</span><span class="sxs-lookup"><span data-stu-id="40f90-148">Scope of the resource.</span></span>
<span data-ttu-id="40f90-149">Yani.</span><span class="sxs-lookup"><span data-stu-id="40f90-149">E.g.</span></span>
<span data-ttu-id="40f90-150">'/Subscriptions/{SubscriptionID}/ResourceGroups/{RgName} '.</span><span class="sxs-lookup"><span data-stu-id="40f90-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="40f90-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="40f90-151">-Confirm</span></span>
<span data-ttu-id="40f90-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40f90-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f90-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f90-153">-WhatIf</span></span>
<span data-ttu-id="40f90-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40f90-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f90-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40f90-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f90-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f90-156">CommonParameters</span></span>
<span data-ttu-id="40f90-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40f90-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f90-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f90-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f90-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40f90-159">INPUTS</span></span>

### <span data-ttu-id="40f90-160">System. String</span><span class="sxs-lookup"><span data-stu-id="40f90-160">System.String</span></span>

### <span data-ttu-id="40f90-161">System. String []</span><span class="sxs-lookup"><span data-stu-id="40f90-161">System.String[]</span></span>

## <span data-ttu-id="40f90-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40f90-162">OUTPUTS</span></span>

### <span data-ttu-id="40f90-163">Microsoft. Azure. Commands. Policınsi. model. düzeltme. Psdüzeltme</span><span class="sxs-lookup"><span data-stu-id="40f90-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="40f90-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40f90-164">NOTES</span></span>

## <span data-ttu-id="40f90-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40f90-165">RELATED LINKS</span></span>
