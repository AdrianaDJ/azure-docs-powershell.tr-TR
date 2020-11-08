---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 867f06722e6840c9bba6065236fbf4f5f5c8b7f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933435"
---
# <span data-ttu-id="70fb9-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="70fb9-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="70fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="70fb9-103">Bir Azure Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="70fb9-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="70fb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70fb9-104">SYNTAX</span></span>

### <span data-ttu-id="70fb9-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70fb9-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70fb9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="70fb9-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70fb9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="70fb9-107">DESCRIPTION</span></span>
<span data-ttu-id="70fb9-108">**Stop-AzRecoveryServicesAsrJob** cmdlet 'ı belirtilen Azure Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="70fb9-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="70fb9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70fb9-109">EXAMPLES</span></span>

### <span data-ttu-id="70fb9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70fb9-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="70fb9-111">Belirtilen işi durdurmaya çalışır ve güncelleştirilmiş bir ASR iş nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="70fb9-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="70fb9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70fb9-112">PARAMETERS</span></span>

### <span data-ttu-id="70fb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fb9-113">-DefaultProfile</span></span>
<span data-ttu-id="70fb9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70fb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="70fb9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70fb9-115">-InputObject</span></span>
<span data-ttu-id="70fb9-116">Giriş nesnesi: ASR işine karşılık gelen ASR iş nesnesini</span><span class="sxs-lookup"><span data-stu-id="70fb9-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="70fb9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="70fb9-117">-Name</span></span>
<span data-ttu-id="70fb9-118">ASR işi adı tarafından durdurulacak ASR Işini belirtin.</span><span class="sxs-lookup"><span data-stu-id="70fb9-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="70fb9-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="70fb9-119">-Confirm</span></span>
<span data-ttu-id="70fb9-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70fb9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70fb9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70fb9-121">-WhatIf</span></span>
<span data-ttu-id="70fb9-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70fb9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70fb9-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70fb9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70fb9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fb9-124">CommonParameters</span></span>
<span data-ttu-id="70fb9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70fb9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fb9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70fb9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fb9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70fb9-127">INPUTS</span></span>

### <span data-ttu-id="70fb9-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="70fb9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="70fb9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70fb9-129">OUTPUTS</span></span>

### <span data-ttu-id="70fb9-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="70fb9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="70fb9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70fb9-131">NOTES</span></span>

## <span data-ttu-id="70fb9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70fb9-132">RELATED LINKS</span></span>

[<span data-ttu-id="70fb9-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="70fb9-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="70fb9-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="70fb9-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="70fb9-135">Özgeçmiş-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="70fb9-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)