---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764790"
---
# <span data-ttu-id="84566-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84566-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="84566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84566-102">SYNOPSIS</span></span>
<span data-ttu-id="84566-103">Kurtarma Hizmetleri kasasından belirtilen ASR kurtarma planını silin.</span><span class="sxs-lookup"><span data-stu-id="84566-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84566-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84566-104">SYNTAX</span></span>

### <span data-ttu-id="84566-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84566-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84566-106">ByName</span><span class="sxs-lookup"><span data-stu-id="84566-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84566-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84566-107">DESCRIPTION</span></span>
<span data-ttu-id="84566-108">**Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="84566-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="84566-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84566-109">EXAMPLES</span></span>

### <span data-ttu-id="84566-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84566-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="84566-111">Belirtilen kurtarma planının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="84566-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="84566-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84566-112">PARAMETERS</span></span>

### <span data-ttu-id="84566-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84566-113">-InputObject</span></span>
<span data-ttu-id="84566-114">Cmdlet 'e giriş nesnesi: kurtarma planına karşılık gelen ASR kurtarma planı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="84566-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84566-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="84566-115">-Name</span></span>
<span data-ttu-id="84566-116">Silinecek kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84566-116">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84566-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="84566-117">-Confirm</span></span>
<span data-ttu-id="84566-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84566-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84566-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84566-119">-WhatIf</span></span>
<span data-ttu-id="84566-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84566-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84566-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84566-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84566-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84566-122">CommonParameters</span></span>
<span data-ttu-id="84566-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84566-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84566-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84566-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84566-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84566-125">INPUTS</span></span>

### <span data-ttu-id="84566-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84566-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="84566-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84566-127">OUTPUTS</span></span>

### <span data-ttu-id="84566-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="84566-128">System.Object</span></span>

## <span data-ttu-id="84566-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84566-129">NOTES</span></span>

## <span data-ttu-id="84566-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84566-130">RELATED LINKS</span></span>

[<span data-ttu-id="84566-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84566-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="84566-132">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84566-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="84566-133">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="84566-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)

