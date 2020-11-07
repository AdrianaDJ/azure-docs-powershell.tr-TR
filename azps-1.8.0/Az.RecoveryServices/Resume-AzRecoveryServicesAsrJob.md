---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 4e8b7cda670a0e67cc635ce52f0934c806733c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759620"
---
# <span data-ttu-id="aa158-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="aa158-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="aa158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa158-102">SYNOPSIS</span></span>
<span data-ttu-id="aa158-103">Askıya alınan Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="aa158-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="aa158-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa158-104">SYNTAX</span></span>

### <span data-ttu-id="aa158-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa158-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa158-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aa158-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa158-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa158-107">DESCRIPTION</span></span>
<span data-ttu-id="aa158-108">**Özgeçmiş-AzRecoveryServicesAsrJob** cmdlet 'i askıya alınan bir Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="aa158-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="aa158-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa158-109">EXAMPLES</span></span>

### <span data-ttu-id="aa158-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa158-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="aa158-111">Bekleme veya askıya alınmış durumdaydı, belirtilen işi sürdürün ve ASR işine karşılık gelen güncelleştirilmiş ASR iş nesnesini geri döndürün.</span><span class="sxs-lookup"><span data-stu-id="aa158-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="aa158-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa158-112">PARAMETERS</span></span>

### <span data-ttu-id="aa158-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="aa158-113">-Comment</span></span>
<span data-ttu-id="aa158-114">İş günlüğü için açıklamalar.</span><span class="sxs-lookup"><span data-stu-id="aa158-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa158-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa158-115">-DefaultProfile</span></span>
<span data-ttu-id="aa158-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa158-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="aa158-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa158-117">-InputObject</span></span>
<span data-ttu-id="aa158-118">Cmdlet 'e giriş nesnesi: işe devam eden ASR Iş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aa158-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="aa158-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa158-119">-Name</span></span>
<span data-ttu-id="aa158-120">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="aa158-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="aa158-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa158-121">-Confirm</span></span>
<span data-ttu-id="aa158-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa158-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa158-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa158-123">-WhatIf</span></span>
<span data-ttu-id="aa158-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa158-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa158-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa158-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa158-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa158-126">CommonParameters</span></span>
<span data-ttu-id="aa158-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa158-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa158-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa158-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa158-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa158-129">INPUTS</span></span>

### <span data-ttu-id="aa158-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="aa158-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="aa158-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa158-131">OUTPUTS</span></span>

### <span data-ttu-id="aa158-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="aa158-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="aa158-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa158-133">NOTES</span></span>

## <span data-ttu-id="aa158-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa158-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa158-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="aa158-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="aa158-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="aa158-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="aa158-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="aa158-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
