---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751867"
---
# <span data-ttu-id="3e713-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="3e713-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="3e713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e713-102">SYNOPSIS</span></span>
<span data-ttu-id="3e713-103">VM 'e atanan "Konuk yapılandırması" türündeki bir girişimin Konuk yapılandırma ilkesi uyumluluk durumu geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="3e713-104">Initiative, "Initiative" tanım türü ilkedir.</span><span class="sxs-lookup"><span data-stu-id="3e713-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="3e713-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e713-105">SYNTAX</span></span>

### <span data-ttu-id="3e713-106">Initivenamescope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e713-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e713-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="3e713-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e713-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e713-108">DESCRIPTION</span></span>
<span data-ttu-id="3e713-109">Get-AzVMGuestPolicyStatusHistory cmdlet, VM 'e atanan "Konuk yapılandırması" türündeki bir girişimin uyumluluk durumu geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="3e713-110">Initiative, "Initiative" tanım türü ilkedir.</span><span class="sxs-lookup"><span data-stu-id="3e713-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="3e713-111">Get-AzVMGuestPolicyStatusHistory cmdlet 'inin çıktısında bulunan ReportId kullanarak tek bir uyumluluk durumunun ayrıntılarını almak için Get-AzVMGuestPolicyStatus cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e713-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="3e713-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e713-112">EXAMPLES</span></span>

### <span data-ttu-id="3e713-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3e713-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="3e713-114">Uyumsuzluk kimliğine göre uyumluluk durumu geçmişini alır. ShowOnlyChange anahtarı yalnızca geçmiş durumu değişikliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e713-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="3e713-115">İki uyumluluk çeki arasında değişmeyen durumları atlar.</span><span class="sxs-lookup"><span data-stu-id="3e713-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="3e713-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3e713-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="3e713-117">Uyumluluk durumu geçmişini Initiative adına göre alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="3e713-118">ShowOnlyChange anahtarı yalnızca geçmiş durumu değişikliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e713-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="3e713-119">İki uyumluluk çeki arasında değişmeyen durumları atlar.</span><span class="sxs-lookup"><span data-stu-id="3e713-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="3e713-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3e713-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="3e713-121">VM 'ye atanan tüm konuk yapılandırma ilkelerinin uyumluluk durumu geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="3e713-122">ShowOnlyChange anahtarı yalnızca geçmiş durumu değişikliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e713-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="3e713-123">İki uyumluluk çeki arasında değişmeyen durumları atlar.</span><span class="sxs-lookup"><span data-stu-id="3e713-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="3e713-124">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="3e713-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="3e713-125">Uyumluluk durumu geçmişini Initiative ID 'ye göre alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="3e713-126">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="3e713-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="3e713-127">Uyumluluk durumu geçmişini Initiative adına göre alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="3e713-128">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="3e713-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="3e713-129">VM 'ye atanan tüm konuk yapılandırma ilkelerinin uyumluluk durumu geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3e713-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="3e713-130">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="3e713-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="3e713-131">ReportId ile Konuk yapılandırma ilkesi durumunu edinin.</span><span class="sxs-lookup"><span data-stu-id="3e713-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="3e713-132">ReportId, Get-Azvmguestpolicypolicy geçmiş sonuçlarında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="3e713-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="3e713-133">(lütfen diğer örneklere bakın)</span><span class="sxs-lookup"><span data-stu-id="3e713-133">(please refer other examples)</span></span>

## <span data-ttu-id="3e713-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e713-134">PARAMETERS</span></span>

### <span data-ttu-id="3e713-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e713-135">-DefaultProfile</span></span>
<span data-ttu-id="3e713-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e713-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e713-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="3e713-137">-InitiativeId</span></span>
<span data-ttu-id="3e713-138">Tanımlama türünün Initiative ve category Konuk yapılandırması olduğu bir ilkenin tanım kimliği</span><span class="sxs-lookup"><span data-stu-id="3e713-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e713-139">-Initikavename</span><span class="sxs-lookup"><span data-stu-id="3e713-139">-InitiativeName</span></span>
<span data-ttu-id="3e713-140">Tanımlama türünün Initiative ve category Konuk yapılandırması olduğu bir ilkenin adı</span><span class="sxs-lookup"><span data-stu-id="3e713-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e713-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e713-141">-ResourceGroupName</span></span>
<span data-ttu-id="3e713-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3e713-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e713-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="3e713-143">-ShowOnlyChange</span></span>
<span data-ttu-id="3e713-144">Yalnızca Konuk yapılandırma ilkeleri için geçmiş durumu değişikliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e713-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="3e713-145">İki uyumluluk durumu denetimi çalışması arasında değişmeyen durumları atlar.</span><span class="sxs-lookup"><span data-stu-id="3e713-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e713-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e713-146">-VMName</span></span>
<span data-ttu-id="3e713-147">VM adı.</span><span class="sxs-lookup"><span data-stu-id="3e713-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e713-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e713-148">CommonParameters</span></span>
<span data-ttu-id="3e713-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e713-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e713-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e713-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e713-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e713-151">INPUTS</span></span>

### <span data-ttu-id="3e713-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3e713-152">None</span></span>
## <span data-ttu-id="3e713-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e713-153">OUTPUTS</span></span>

### <span data-ttu-id="3e713-154">Microsoft. Azure. Commands. GuestConfiguration. modeller. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="3e713-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="3e713-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e713-155">NOTES</span></span>

## <span data-ttu-id="3e713-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e713-156">RELATED LINKS</span></span>
