---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c5efb6b9aa7d78ef5f8d50ef80c5155c7e731f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593657"
---
# <span data-ttu-id="a8ed4-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a8ed4-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="a8ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ed4-103">Askıya alınan Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ed4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8ed4-104">SYNTAX</span></span>

### <span data-ttu-id="a8ed4-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8ed4-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ed4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a8ed4-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ed4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8ed4-107">DESCRIPTION</span></span>
<span data-ttu-id="a8ed4-108">**Özgeçmiş-AzureRmRecoveryServicesAsrJob** cmdlet 'i askıya alınan bir Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="a8ed4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8ed4-109">EXAMPLES</span></span>

### <span data-ttu-id="a8ed4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8ed4-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="a8ed4-111">Bekleme veya askıya alınmış durumdaydı, belirtilen işi sürdürün ve ASR işine karşılık gelen güncelleştirilmiş ASR iş nesnesini geri döndürün.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="a8ed4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8ed4-112">PARAMETERS</span></span>

### <span data-ttu-id="a8ed4-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a8ed4-113">-Comment</span></span>
<span data-ttu-id="a8ed4-114">İş günlüğü için açıklamalar.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="a8ed4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ed4-115">-DefaultProfile</span></span>
<span data-ttu-id="a8ed4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ed4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ed4-117">-InputObject</span></span>
<span data-ttu-id="a8ed4-118">Cmdlet 'e giriş nesnesi: işe devam eden ASR Iş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="a8ed4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8ed4-119">-Name</span></span>
<span data-ttu-id="a8ed4-120">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="a8ed4-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8ed4-121">-Confirm</span></span>
<span data-ttu-id="a8ed4-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ed4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ed4-123">-WhatIf</span></span>
<span data-ttu-id="a8ed4-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8ed4-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ed4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ed4-126">CommonParameters</span></span>
<span data-ttu-id="a8ed4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8ed4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ed4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ed4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ed4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8ed4-129">INPUTS</span></span>

### <span data-ttu-id="a8ed4-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a8ed4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a8ed4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8ed4-131">OUTPUTS</span></span>

### <span data-ttu-id="a8ed4-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a8ed4-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a8ed4-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8ed4-133">NOTES</span></span>

## <span data-ttu-id="a8ed4-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8ed4-134">RELATED LINKS</span></span>

[<span data-ttu-id="a8ed4-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a8ed4-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="a8ed4-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a8ed4-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="a8ed4-137">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a8ed4-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
