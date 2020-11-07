---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763650"
---
# <span data-ttu-id="faa0f-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="faa0f-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="faa0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faa0f-102">SYNOPSIS</span></span>
<span data-ttu-id="faa0f-103">Bir Azure Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="faa0f-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faa0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faa0f-104">SYNTAX</span></span>

### <span data-ttu-id="faa0f-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="faa0f-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa0f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="faa0f-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faa0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="faa0f-107">DESCRIPTION</span></span>
<span data-ttu-id="faa0f-108">**Stop-AzureRmRecoveryServicesAsrJob** cmdlet 'ı belirtilen Azure Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="faa0f-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="faa0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faa0f-109">EXAMPLES</span></span>

### <span data-ttu-id="faa0f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="faa0f-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="faa0f-111">Belirtilen işi durdurmaya çalışır ve güncelleştirilmiş bir ASR iş nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="faa0f-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="faa0f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faa0f-112">PARAMETERS</span></span>

### <span data-ttu-id="faa0f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faa0f-113">-InputObject</span></span>
<span data-ttu-id="faa0f-114">Giriş nesnesi: ASR işine karşılık gelen ASR iş nesnesini</span><span class="sxs-lookup"><span data-stu-id="faa0f-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="faa0f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="faa0f-115">-Name</span></span>
<span data-ttu-id="faa0f-116">ASR işi adı tarafından durdurulacak ASR Işini belirtin.</span><span class="sxs-lookup"><span data-stu-id="faa0f-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="faa0f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="faa0f-117">-Confirm</span></span>
<span data-ttu-id="faa0f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="faa0f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa0f-119">-WhatIf</span></span>
<span data-ttu-id="faa0f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="faa0f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faa0f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="faa0f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa0f-122">CommonParameters</span></span>
<span data-ttu-id="faa0f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faa0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa0f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa0f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faa0f-125">INPUTS</span></span>

### <span data-ttu-id="faa0f-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="faa0f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="faa0f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faa0f-127">OUTPUTS</span></span>

### <span data-ttu-id="faa0f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="faa0f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="faa0f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faa0f-129">NOTES</span></span>

## <span data-ttu-id="faa0f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faa0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="faa0f-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="faa0f-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="faa0f-132">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="faa0f-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="faa0f-133">Özgeçmiş-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="faa0f-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
