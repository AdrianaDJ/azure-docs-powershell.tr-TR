---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593037"
---
# <span data-ttu-id="7e33b-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7e33b-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="7e33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e33b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e33b-103">Askıya alınan Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="7e33b-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e33b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e33b-104">SYNTAX</span></span>

### <span data-ttu-id="7e33b-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e33b-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e33b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7e33b-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e33b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e33b-107">DESCRIPTION</span></span>
<span data-ttu-id="7e33b-108">**Özgeçmiş-AzureRmRecoveryServicesAsrJob** cmdlet 'i askıya alınan bir Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="7e33b-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="7e33b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e33b-109">EXAMPLES</span></span>

### <span data-ttu-id="7e33b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e33b-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="7e33b-111">Bekleme veya askıya alınmış durumdaydı, belirtilen işi sürdürün ve ASR işine karşılık gelen güncelleştirilmiş ASR iş nesnesini geri döndürün.</span><span class="sxs-lookup"><span data-stu-id="7e33b-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="7e33b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e33b-112">PARAMETERS</span></span>

### <span data-ttu-id="7e33b-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7e33b-113">-Comment</span></span>
<span data-ttu-id="7e33b-114">İş günlüğü için açıklamalar.</span><span class="sxs-lookup"><span data-stu-id="7e33b-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e33b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e33b-115">-InputObject</span></span>
<span data-ttu-id="7e33b-116">Cmdlet 'e giriş nesnesi: işe devam eden ASR Iş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7e33b-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e33b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e33b-117">-Name</span></span>
<span data-ttu-id="7e33b-118">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e33b-118">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="7e33b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e33b-119">-Confirm</span></span>
<span data-ttu-id="7e33b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e33b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e33b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e33b-121">-WhatIf</span></span>
<span data-ttu-id="7e33b-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e33b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e33b-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e33b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e33b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e33b-124">CommonParameters</span></span>
<span data-ttu-id="7e33b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e33b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e33b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e33b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e33b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e33b-127">INPUTS</span></span>

### <span data-ttu-id="7e33b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7e33b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7e33b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e33b-129">OUTPUTS</span></span>

### <span data-ttu-id="7e33b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7e33b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7e33b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e33b-131">NOTES</span></span>

## <span data-ttu-id="7e33b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e33b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e33b-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7e33b-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="7e33b-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7e33b-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="7e33b-135">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7e33b-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
