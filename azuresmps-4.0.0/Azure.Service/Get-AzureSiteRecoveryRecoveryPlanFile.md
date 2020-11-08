---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105583"
---
# <span data-ttu-id="4ef14-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="4ef14-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="4ef14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef14-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef14-103">Bir Azure Site kurtarma planını XML biçiminde yükler.</span><span class="sxs-lookup"><span data-stu-id="4ef14-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="4ef14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ef14-104">SYNTAX</span></span>

### <span data-ttu-id="4ef14-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ef14-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4ef14-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="4ef14-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ef14-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef14-108">**Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet 'i, bir Azure Site Recovery planını XML biçiminde yükler.</span><span class="sxs-lookup"><span data-stu-id="4ef14-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="4ef14-109">Kurtarma planını güncelleştirmek ve site kurtarma sunucusuna yüklemek için bu dosyayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ef14-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="4ef14-110">Kurtarma planı bir gruptaki sanal makineleri, yük devretme ve kurtarma amacıyla alır.</span><span class="sxs-lookup"><span data-stu-id="4ef14-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="4ef14-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ef14-111">EXAMPLES</span></span>

### <span data-ttu-id="4ef14-112">Örnek 1: kurtarma planı dosyası alma</span><span class="sxs-lookup"><span data-stu-id="4ef14-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="4ef14-113">Bu komut **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ini kullanarak kurtarma planını alır ve $RecoveryPlan değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4ef14-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="4ef14-114">İkinci komut, $RecoveryPlan Site Recovery planı XML dosyasını almak için **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4ef14-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="4ef14-115">Komut, XML dosyasını belirtilen yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="4ef14-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="4ef14-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ef14-116">PARAMETERS</span></span>

### <span data-ttu-id="4ef14-117">-ID</span><span class="sxs-lookup"><span data-stu-id="4ef14-117">-Id</span></span>
<span data-ttu-id="4ef14-118">Alınacak kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef14-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="4ef14-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="4ef14-119">-Path</span></span>
<span data-ttu-id="4ef14-120">Kurtarma planı XML dosyasının depolanacağı tam yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef14-120">Specifies the full path to store the recovery plan XML file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="4ef14-121">-Profile</span></span>
<span data-ttu-id="4ef14-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef14-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4ef14-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4ef14-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4ef14-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ef14-124">-RecoveryPlan</span></span>
<span data-ttu-id="4ef14-125">Kurtarma planının alınacağı bir **Asrrecoveryplan** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef14-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="4ef14-126">Bir **Asrrecoveryplan** nesnesi almak Için, **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4ef14-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef14-127">CommonParameters</span></span>
<span data-ttu-id="4ef14-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ef14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef14-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef14-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef14-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ef14-130">INPUTS</span></span>

## <span data-ttu-id="4ef14-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ef14-131">OUTPUTS</span></span>

## <span data-ttu-id="4ef14-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ef14-132">NOTES</span></span>

## <span data-ttu-id="4ef14-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ef14-133">RELATED LINKS</span></span>

[<span data-ttu-id="4ef14-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4ef14-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


