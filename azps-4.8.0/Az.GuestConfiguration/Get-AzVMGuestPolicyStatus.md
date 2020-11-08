---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108266"
---
# <span data-ttu-id="16565-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="16565-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="16565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16565-102">SYNOPSIS</span></span>
<span data-ttu-id="16565-103">VM 'e atanan "Konuk yapılandırması" türünde bir girişimin Konuk yapılandırma ilkesi durumlarını (ayrıntılı) alır.</span><span class="sxs-lookup"><span data-stu-id="16565-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="16565-104">Initiative, "Initiative" tanım türü ilkedir.</span><span class="sxs-lookup"><span data-stu-id="16565-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="16565-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16565-105">SYNTAX</span></span>

### <span data-ttu-id="16565-106">VmScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16565-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16565-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="16565-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16565-108">Initivenamescope</span><span class="sxs-lookup"><span data-stu-id="16565-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16565-109">Reporsscope</span><span class="sxs-lookup"><span data-stu-id="16565-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16565-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="16565-110">DESCRIPTION</span></span>
<span data-ttu-id="16565-111">Get-AzVMGuestPolicyStatus cmdlet, VM 'e atanan "Konuk yapılandırması" türünde bir girişimin Konuk yapılandırma ilkesi durumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="16565-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="16565-112">Initiative, "Initiative" tanım türü ilkedir.</span><span class="sxs-lookup"><span data-stu-id="16565-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="16565-113">Bu cmdlet, VM 'deki uyumluluk durumlarını ve girişimdeki bireysel ilkeler için uyumlu olmama nedenlerini alır.</span><span class="sxs-lookup"><span data-stu-id="16565-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="16565-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16565-114">EXAMPLES</span></span>

### <span data-ttu-id="16565-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16565-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="16565-116">VM için tüm en son Konuk yapılandırma ilkesi durumlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="16565-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="16565-117">Durum, uyumluluk için denetlenen kaynak bilgilerinin "Konuk yapılandırması" türündeki tüm girişimlerdeki her ilke için VM 'in uyumluluk durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="16565-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="16565-118">Sonuçlar en son durumları içerir, önceki geçmiş durumları içermez.</span><span class="sxs-lookup"><span data-stu-id="16565-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="16565-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="16565-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="16565-120">En son Konuk yapılandırması ilke durumlarını Initiative ID ile alın. Durum, girişimdeki her ilke için VM 'in uyumluluk durumunu, uyumluluk nedenlerini, uyumluluk denetiminin süresini, uyumluluk için denetlenen kaynak bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="16565-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="16565-121">Sonuçlar önceki durumların üretilmediğinden, girişimdeki her ilkeye ilişkin en son durumu içerir.</span><span class="sxs-lookup"><span data-stu-id="16565-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="16565-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="16565-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="16565-123">En son Konuk yapılandırması ilke durumlarını Initiative adına göre edinin.</span><span class="sxs-lookup"><span data-stu-id="16565-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="16565-124">Durum, girişimdeki her ilke için VM 'in uyumluluk durumunu, uyumluluk nedenlerini, uyumluluk denetiminin süresini, uyumluluk için denetlenen kaynak bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="16565-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="16565-125">Sonuçlar önceki durumların üretilmediğinden, girişimdeki her ilkeye ilişkin en son durumu içerir.</span><span class="sxs-lookup"><span data-stu-id="16565-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="16565-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="16565-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="16565-127">ReportId ile Konuk yapılandırma ilkesi durumunu edinin.</span><span class="sxs-lookup"><span data-stu-id="16565-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="16565-128">ReportId, initiativeId veya Initiative adına göre Get-AzVMGuestPolicyStatus sonuçlarında bulunan ReportId özelliğidir (lütfen diğer örneklere bakın)</span><span class="sxs-lookup"><span data-stu-id="16565-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="16565-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16565-129">PARAMETERS</span></span>

### <span data-ttu-id="16565-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16565-130">-DefaultProfile</span></span>
<span data-ttu-id="16565-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16565-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16565-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="16565-132">-InitiativeId</span></span>
<span data-ttu-id="16565-133">Tanımlama türünün Initiative ve category Konuk yapılandırması olduğu bir ilkenin tanım kimliği</span><span class="sxs-lookup"><span data-stu-id="16565-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16565-134">-Initikavename</span><span class="sxs-lookup"><span data-stu-id="16565-134">-InitiativeName</span></span>
<span data-ttu-id="16565-135">Tanımlama türünün Initiative ve category Konuk yapılandırması olduğu bir ilkenin adı</span><span class="sxs-lookup"><span data-stu-id="16565-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="16565-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="16565-136">-ReportId</span></span>
<span data-ttu-id="16565-137">Konuk yapılandırma ilkesinin durumu.</span><span class="sxs-lookup"><span data-stu-id="16565-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="16565-138">Tanımlama türünün Initiative ve category olduğu bir ilke, durumları almak için bir kapsama atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16565-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16565-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16565-139">-ResourceGroupName</span></span>
<span data-ttu-id="16565-140">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16565-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16565-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="16565-141">-VMName</span></span>
<span data-ttu-id="16565-142">VM adı.</span><span class="sxs-lookup"><span data-stu-id="16565-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16565-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16565-143">CommonParameters</span></span>
<span data-ttu-id="16565-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16565-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16565-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16565-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16565-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16565-146">INPUTS</span></span>

### <span data-ttu-id="16565-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="16565-147">None</span></span>
## <span data-ttu-id="16565-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16565-148">OUTPUTS</span></span>

### <span data-ttu-id="16565-149">Microsoft. Azure. Commands. GuestConfiguration. modeller. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="16565-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="16565-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16565-150">NOTES</span></span>

## <span data-ttu-id="16565-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16565-151">RELATED LINKS</span></span>
