---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4931b32cf2c74180ad06b071d19ef57f4be2285e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759637"
---
# <span data-ttu-id="16e15-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e15-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="16e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e15-102">SYNOPSIS</span></span>
<span data-ttu-id="16e15-103">Belirtilen ASR kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="16e15-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="16e15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16e15-104">SYNTAX</span></span>

### <span data-ttu-id="16e15-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16e15-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e15-106">ByName</span><span class="sxs-lookup"><span data-stu-id="16e15-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e15-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="16e15-107">DESCRIPTION</span></span>
<span data-ttu-id="16e15-108">**Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="16e15-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="16e15-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16e15-109">EXAMPLES</span></span>

### <span data-ttu-id="16e15-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16e15-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="16e15-111">Belirtilen kurtarma planının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16e15-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="16e15-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16e15-112">PARAMETERS</span></span>

### <span data-ttu-id="16e15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e15-113">-DefaultProfile</span></span>
<span data-ttu-id="16e15-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16e15-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="16e15-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e15-115">-InputObject</span></span>
<span data-ttu-id="16e15-116">Cmdlet 'e giriş nesnesi: kurtarma planına karşılık gelen ASR kurtarma planı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="16e15-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16e15-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="16e15-117">-Name</span></span>
<span data-ttu-id="16e15-118">Silinecek kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16e15-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e15-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="16e15-119">-Confirm</span></span>
<span data-ttu-id="16e15-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16e15-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e15-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e15-121">-WhatIf</span></span>
<span data-ttu-id="16e15-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16e15-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e15-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16e15-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e15-124">CommonParameters</span></span>
<span data-ttu-id="16e15-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16e15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e15-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e15-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e15-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16e15-127">INPUTS</span></span>

### <span data-ttu-id="16e15-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e15-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="16e15-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16e15-129">OUTPUTS</span></span>

### <span data-ttu-id="16e15-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="16e15-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="16e15-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16e15-131">NOTES</span></span>

## <span data-ttu-id="16e15-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16e15-132">RELATED LINKS</span></span>

[<span data-ttu-id="16e15-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e15-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="16e15-134">Yeni-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e15-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="16e15-135">Güncelleştirme-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e15-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


