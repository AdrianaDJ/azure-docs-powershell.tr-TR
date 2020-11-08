---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103535"
---
# <span data-ttu-id="c64c4-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c64c4-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c64c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c64c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c64c4-103">Azure Site kurtarma işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c64c4-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="c64c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c64c4-104">SYNTAX</span></span>

### <span data-ttu-id="c64c4-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c64c4-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c64c4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c64c4-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c64c4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c64c4-107">DESCRIPTION</span></span>
<span data-ttu-id="c64c4-108">**Restart-AzRecoveryServicesAsrJob** cmdlet 'ı bir Azure Site Recovery işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c64c4-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="c64c4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c64c4-109">EXAMPLES</span></span>

### <span data-ttu-id="c64c4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c64c4-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="c64c4-111">Belirtilen ASR işini yeniden başlatır ve ASR işinin güncelleştirilmiş ASR işi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c64c4-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="c64c4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c64c4-112">PARAMETERS</span></span>

### <span data-ttu-id="c64c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64c4-113">-DefaultProfile</span></span>
<span data-ttu-id="c64c4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c64c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c64c4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c64c4-115">-InputObject</span></span>
<span data-ttu-id="c64c4-116">Cmdlet 'e giriş nesnesi: ASR işine karşılık gelen ASR iş nesnesi</span><span class="sxs-lookup"><span data-stu-id="c64c4-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c64c4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c64c4-117">-Name</span></span>
<span data-ttu-id="c64c4-118">İşi adıyla belirtin.</span><span class="sxs-lookup"><span data-stu-id="c64c4-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="c64c4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c64c4-119">-Confirm</span></span>
<span data-ttu-id="c64c4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c64c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c64c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c64c4-121">-WhatIf</span></span>
<span data-ttu-id="c64c4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c64c4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c64c4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c64c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c64c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64c4-124">CommonParameters</span></span>
<span data-ttu-id="c64c4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c64c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64c4-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c64c4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64c4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c64c4-127">INPUTS</span></span>

### <span data-ttu-id="c64c4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c64c4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c64c4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c64c4-129">OUTPUTS</span></span>

### <span data-ttu-id="c64c4-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c64c4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c64c4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c64c4-131">NOTES</span></span>

## <span data-ttu-id="c64c4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c64c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="c64c4-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c64c4-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c64c4-134">Özgeçmiş-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c64c4-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c64c4-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c64c4-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
