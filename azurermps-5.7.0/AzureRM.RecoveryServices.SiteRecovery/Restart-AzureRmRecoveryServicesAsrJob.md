---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 0ac09a527aff78648d3af14413baa33da137d59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589729"
---
# <span data-ttu-id="bd58a-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bd58a-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="bd58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd58a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd58a-103">Azure Site kurtarma işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="bd58a-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd58a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd58a-104">SYNTAX</span></span>

### <span data-ttu-id="bd58a-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd58a-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd58a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bd58a-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd58a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd58a-107">DESCRIPTION</span></span>
<span data-ttu-id="bd58a-108">**Restart-AzureRmRecoveryServicesAsrJob** cmdlet 'ı bir Azure Site Recovery işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="bd58a-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="bd58a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd58a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd58a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd58a-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="bd58a-111">Belirtilen ASR işini yeniden başlatır ve ASR işinin güncelleştirilmiş ASR işi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bd58a-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="bd58a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd58a-112">PARAMETERS</span></span>

### <span data-ttu-id="bd58a-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd58a-113">-Confirm</span></span>
<span data-ttu-id="bd58a-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd58a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd58a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd58a-115">-DefaultProfile</span></span>
<span data-ttu-id="bd58a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd58a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd58a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd58a-117">-InputObject</span></span>
<span data-ttu-id="bd58a-118">Cmdlet 'e giriş nesnesi: ASR işine karşılık gelen ASR iş nesnesi</span><span class="sxs-lookup"><span data-stu-id="bd58a-118">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="bd58a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd58a-119">-Name</span></span>
<span data-ttu-id="bd58a-120">İşi adıyla belirtin.</span><span class="sxs-lookup"><span data-stu-id="bd58a-120">Specify the job by name.</span></span>

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

### <span data-ttu-id="bd58a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd58a-121">-WhatIf</span></span>
<span data-ttu-id="bd58a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd58a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd58a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd58a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd58a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd58a-124">CommonParameters</span></span>
<span data-ttu-id="bd58a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd58a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd58a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd58a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd58a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd58a-127">INPUTS</span></span>

### <span data-ttu-id="bd58a-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bd58a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bd58a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd58a-129">OUTPUTS</span></span>

### <span data-ttu-id="bd58a-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bd58a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bd58a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd58a-131">NOTES</span></span>

## <span data-ttu-id="bd58a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd58a-132">RELATED LINKS</span></span>

[<span data-ttu-id="bd58a-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bd58a-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="bd58a-134">Özgeçmiş-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bd58a-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="bd58a-135">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bd58a-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
