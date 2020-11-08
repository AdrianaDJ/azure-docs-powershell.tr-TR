---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106076"
---
# <span data-ttu-id="d8e68-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8e68-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="d8e68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e68-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e68-103">Site kurtarma işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d8e68-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="d8e68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8e68-104">SYNTAX</span></span>

### <span data-ttu-id="d8e68-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8e68-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8e68-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="d8e68-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8e68-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8e68-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e68-108">**Restart-AzureSiteRecoveryJob** cmdlet 'ı bir Azure Site Recovery işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d8e68-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d8e68-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8e68-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e68-110">Örnek 1: işi yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="d8e68-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="d8e68-111">Bu komut belirtilen KIMLIĞE sahip işi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d8e68-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="d8e68-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8e68-112">PARAMETERS</span></span>

### <span data-ttu-id="d8e68-113">-ID</span><span class="sxs-lookup"><span data-stu-id="d8e68-113">-Id</span></span>
<span data-ttu-id="d8e68-114">Yeniden başlatılacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8e68-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="d8e68-115">-Job</span><span class="sxs-lookup"><span data-stu-id="d8e68-115">-Job</span></span>
<span data-ttu-id="d8e68-116">Yeniden başlatılacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8e68-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="d8e68-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8e68-117">-Profile</span></span>
<span data-ttu-id="d8e68-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8e68-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8e68-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d8e68-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8e68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e68-120">CommonParameters</span></span>
<span data-ttu-id="d8e68-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8e68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e68-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e68-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e68-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8e68-123">INPUTS</span></span>

## <span data-ttu-id="d8e68-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8e68-124">OUTPUTS</span></span>

## <span data-ttu-id="d8e68-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8e68-125">NOTES</span></span>

## <span data-ttu-id="d8e68-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8e68-126">RELATED LINKS</span></span>

[<span data-ttu-id="d8e68-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8e68-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d8e68-128">Özgeçmiş-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8e68-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d8e68-129">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8e68-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


