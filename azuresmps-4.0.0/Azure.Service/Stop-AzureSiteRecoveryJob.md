---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106407"
---
# <span data-ttu-id="18f34-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="18f34-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="18f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f34-102">SYNOPSIS</span></span>
<span data-ttu-id="18f34-103">Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="18f34-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="18f34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18f34-104">SYNTAX</span></span>

### <span data-ttu-id="18f34-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18f34-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="18f34-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="18f34-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="18f34-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18f34-107">DESCRIPTION</span></span>
<span data-ttu-id="18f34-108">**Stop-AzureSiteRecoveryJob** cmdlet 'ı bir Azure Site Recovery işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="18f34-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="18f34-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18f34-109">EXAMPLES</span></span>

### <span data-ttu-id="18f34-110">Örnek 1: tüm işleri durdurma</span><span class="sxs-lookup"><span data-stu-id="18f34-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="18f34-111">İlk komut **Get-AzureSiteRecoveryJob** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası Için Azure Site kurtarma işlerini alır ve sonuçları $Jobs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="18f34-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="18f34-112">İkinci komut $Jobs tarafından belirtilen işleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="18f34-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="18f34-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18f34-113">PARAMETERS</span></span>

### <span data-ttu-id="18f34-114">-ID</span><span class="sxs-lookup"><span data-stu-id="18f34-114">-Id</span></span>
<span data-ttu-id="18f34-115">Durdurulacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f34-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="18f34-116">-Job</span><span class="sxs-lookup"><span data-stu-id="18f34-116">-Job</span></span>
<span data-ttu-id="18f34-117">Durdurulacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f34-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="18f34-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="18f34-118">-Profile</span></span>
<span data-ttu-id="18f34-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f34-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18f34-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="18f34-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18f34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f34-121">CommonParameters</span></span>
<span data-ttu-id="18f34-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18f34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f34-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f34-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f34-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18f34-124">INPUTS</span></span>

## <span data-ttu-id="18f34-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18f34-125">OUTPUTS</span></span>

## <span data-ttu-id="18f34-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18f34-126">NOTES</span></span>

## <span data-ttu-id="18f34-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18f34-127">RELATED LINKS</span></span>

[<span data-ttu-id="18f34-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="18f34-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="18f34-129">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="18f34-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="18f34-130">Özgeçmiş-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="18f34-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


