---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589155"
---
# <span data-ttu-id="caa09-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="caa09-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="caa09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caa09-102">SYNOPSIS</span></span>
<span data-ttu-id="caa09-103">Belirtilen ASR çoğaltma ilkesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="caa09-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="caa09-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caa09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="caa09-105">DESCRIPTION</span></span>
<span data-ttu-id="caa09-106">**Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen çoğaltma ilkesini sildi.</span><span class="sxs-lookup"><span data-stu-id="caa09-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="caa09-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="caa09-107">EXAMPLES</span></span>

### <span data-ttu-id="caa09-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="caa09-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="caa09-109">Belirtilen çoğaltma ilkesini silme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="caa09-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="caa09-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="caa09-110">PARAMETERS</span></span>

### <span data-ttu-id="caa09-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caa09-111">-InputObject</span></span>
<span data-ttu-id="caa09-112">Cmdlet 'e giriş nesnesi: silinecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="caa09-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caa09-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="caa09-113">-Confirm</span></span>
<span data-ttu-id="caa09-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="caa09-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa09-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa09-115">-WhatIf</span></span>
<span data-ttu-id="caa09-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="caa09-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="caa09-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="caa09-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa09-118">CommonParameters</span></span>
<span data-ttu-id="caa09-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="caa09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa09-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa09-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa09-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="caa09-121">INPUTS</span></span>

### <span data-ttu-id="caa09-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="caa09-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="caa09-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="caa09-123">OUTPUTS</span></span>

### <span data-ttu-id="caa09-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="caa09-124">System.Object</span></span>

## <span data-ttu-id="caa09-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="caa09-125">NOTES</span></span>

## <span data-ttu-id="caa09-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="caa09-126">RELATED LINKS</span></span>

[<span data-ttu-id="caa09-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="caa09-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="caa09-128">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="caa09-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
