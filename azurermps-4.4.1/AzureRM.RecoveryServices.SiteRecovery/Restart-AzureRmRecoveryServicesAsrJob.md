---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763654"
---
# <span data-ttu-id="0aff8-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0aff8-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0aff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aff8-102">SYNOPSIS</span></span>
<span data-ttu-id="0aff8-103">Azure Site kurtarma işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="0aff8-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aff8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0aff8-104">SYNTAX</span></span>

### <span data-ttu-id="0aff8-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0aff8-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aff8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0aff8-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aff8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0aff8-107">DESCRIPTION</span></span>
<span data-ttu-id="0aff8-108">**Restart-AzureRmRecoveryServicesAsrJob** cmdlet 'ı bir Azure Site Recovery işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="0aff8-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="0aff8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0aff8-109">EXAMPLES</span></span>

### <span data-ttu-id="0aff8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0aff8-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="0aff8-111">Belirtilen ASR işini yeniden başlatır ve ASR işinin güncelleştirilmiş ASR işi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0aff8-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="0aff8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0aff8-112">PARAMETERS</span></span>

### <span data-ttu-id="0aff8-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aff8-113">-InputObject</span></span>
<span data-ttu-id="0aff8-114">Cmdlet 'e giriş nesnesi: ASR işine karşılık gelen ASR iş nesnesi</span><span class="sxs-lookup"><span data-stu-id="0aff8-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="0aff8-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0aff8-115">-Name</span></span>
<span data-ttu-id="0aff8-116">İşi adıyla belirtin.</span><span class="sxs-lookup"><span data-stu-id="0aff8-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="0aff8-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="0aff8-117">-Confirm</span></span>
<span data-ttu-id="0aff8-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0aff8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aff8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aff8-119">-WhatIf</span></span>
<span data-ttu-id="0aff8-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0aff8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0aff8-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0aff8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aff8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aff8-122">CommonParameters</span></span>
<span data-ttu-id="0aff8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0aff8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aff8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aff8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aff8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0aff8-125">INPUTS</span></span>

### <span data-ttu-id="0aff8-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0aff8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0aff8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0aff8-127">OUTPUTS</span></span>

### <span data-ttu-id="0aff8-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0aff8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0aff8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0aff8-129">NOTES</span></span>

## <span data-ttu-id="0aff8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0aff8-130">RELATED LINKS</span></span>

[<span data-ttu-id="0aff8-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0aff8-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="0aff8-132">Özgeçmiş-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0aff8-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="0aff8-133">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0aff8-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
