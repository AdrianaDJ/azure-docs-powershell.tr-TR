---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106440"
---
# <span data-ttu-id="44894-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="44894-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="44894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44894-102">SYNOPSIS</span></span>
<span data-ttu-id="44894-103">Askıya alınan bir site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="44894-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="44894-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44894-104">SYNTAX</span></span>

### <span data-ttu-id="44894-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44894-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="44894-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="44894-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44894-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44894-107">DESCRIPTION</span></span>
<span data-ttu-id="44894-108">**Resume-AzureSiteRecoveryJob** cmdlet 'i askıya alınmış bir Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="44894-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="44894-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44894-109">EXAMPLES</span></span>

### <span data-ttu-id="44894-110">Örnek 1: tüm işleri Sürdür</span><span class="sxs-lookup"><span data-stu-id="44894-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="44894-111">İlk komut **Get-AzureSiteRecoveryJob** cmdlet 'ini kullanarak geçerli site kurtarma Kasası Için tüm Azure Site kurtarma işlerini alır ve sonuçları $Jobs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="44894-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="44894-112">İkinci komut $Jobs belirtilen işi sürdürür.</span><span class="sxs-lookup"><span data-stu-id="44894-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="44894-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44894-113">PARAMETERS</span></span>

### <span data-ttu-id="44894-114">-Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="44894-114">-Comments</span></span>
<span data-ttu-id="44894-115">İş günlüğü için açıklamaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="44894-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44894-116">-ID</span><span class="sxs-lookup"><span data-stu-id="44894-116">-Id</span></span>
<span data-ttu-id="44894-117">Devam etmek için bir iş KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="44894-117">Specifies the ID of a job to resume.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44894-118">-Job</span><span class="sxs-lookup"><span data-stu-id="44894-118">-Job</span></span>
<span data-ttu-id="44894-119">Devam edilecek işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="44894-119">Specifies the job to resume.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44894-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="44894-120">-Profile</span></span>
<span data-ttu-id="44894-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44894-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44894-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="44894-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44894-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44894-123">CommonParameters</span></span>
<span data-ttu-id="44894-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44894-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44894-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44894-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44894-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44894-126">INPUTS</span></span>

## <span data-ttu-id="44894-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44894-127">OUTPUTS</span></span>

## <span data-ttu-id="44894-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44894-128">NOTES</span></span>

## <span data-ttu-id="44894-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44894-129">RELATED LINKS</span></span>

[<span data-ttu-id="44894-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="44894-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="44894-131">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="44894-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="44894-132">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="44894-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


