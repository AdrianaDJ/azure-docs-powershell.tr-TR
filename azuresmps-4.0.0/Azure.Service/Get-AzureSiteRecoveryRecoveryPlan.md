---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105585"
---
# <span data-ttu-id="d91b7-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d91b7-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="d91b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d91b7-103">Site kurtarma 'da kurtarma planı alır.</span><span class="sxs-lookup"><span data-stu-id="d91b7-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="d91b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d91b7-104">SYNTAX</span></span>

### <span data-ttu-id="d91b7-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d91b7-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d91b7-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="d91b7-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d91b7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d91b7-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d91b7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d91b7-108">DESCRIPTION</span></span>
<span data-ttu-id="d91b7-109">**Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ı Azure Site Recovery 'de bir kurtarma planı alır.</span><span class="sxs-lookup"><span data-stu-id="d91b7-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="d91b7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d91b7-110">EXAMPLES</span></span>

### <span data-ttu-id="d91b7-111">Örnek 1: kurtarma planı alma</span><span class="sxs-lookup"><span data-stu-id="d91b7-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="d91b7-112">Bu komut, geçerli Azure Site Recovery Kasası için kurtarma planı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d91b7-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d91b7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d91b7-113">PARAMETERS</span></span>

### <span data-ttu-id="d91b7-114">-ID</span><span class="sxs-lookup"><span data-stu-id="d91b7-114">-Id</span></span>
<span data-ttu-id="d91b7-115">Alınacak kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d91b7-115">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="d91b7-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d91b7-116">-Name</span></span>
<span data-ttu-id="d91b7-117">Alınacak kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d91b7-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="d91b7-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="d91b7-118">-Profile</span></span>
<span data-ttu-id="d91b7-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d91b7-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d91b7-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d91b7-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d91b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91b7-121">CommonParameters</span></span>
<span data-ttu-id="d91b7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d91b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91b7-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d91b7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91b7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d91b7-124">INPUTS</span></span>

## <span data-ttu-id="d91b7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d91b7-125">OUTPUTS</span></span>

## <span data-ttu-id="d91b7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d91b7-126">NOTES</span></span>

## <span data-ttu-id="d91b7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d91b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="d91b7-128">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d91b7-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d91b7-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d91b7-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="d91b7-130">Güncelleştirme-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d91b7-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


