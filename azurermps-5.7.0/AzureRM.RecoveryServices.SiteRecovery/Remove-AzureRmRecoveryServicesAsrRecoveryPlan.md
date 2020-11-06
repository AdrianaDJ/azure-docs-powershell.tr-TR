---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589737"
---
# <span data-ttu-id="28c28-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c28-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="28c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28c28-102">SYNOPSIS</span></span>
<span data-ttu-id="28c28-103">Belirtilen ASR kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="28c28-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28c28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28c28-104">SYNTAX</span></span>

### <span data-ttu-id="28c28-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28c28-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c28-106">ByName</span><span class="sxs-lookup"><span data-stu-id="28c28-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c28-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="28c28-107">DESCRIPTION</span></span>
<span data-ttu-id="28c28-108">**Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="28c28-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="28c28-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28c28-109">EXAMPLES</span></span>

### <span data-ttu-id="28c28-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="28c28-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="28c28-111">Belirtilen kurtarma planının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="28c28-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28c28-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28c28-112">PARAMETERS</span></span>

### <span data-ttu-id="28c28-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="28c28-113">-Confirm</span></span>
<span data-ttu-id="28c28-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28c28-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c28-115">-DefaultProfile</span></span>
<span data-ttu-id="28c28-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28c28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="28c28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28c28-117">-InputObject</span></span>
<span data-ttu-id="28c28-118">Cmdlet 'e giriş nesnesi: kurtarma planına karşılık gelen ASR kurtarma planı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="28c28-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28c28-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="28c28-119">-Name</span></span>
<span data-ttu-id="28c28-120">Silinecek kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28c28-120">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="28c28-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c28-121">-WhatIf</span></span>
<span data-ttu-id="28c28-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28c28-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28c28-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28c28-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c28-124">CommonParameters</span></span>
<span data-ttu-id="28c28-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28c28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c28-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c28-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c28-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28c28-127">INPUTS</span></span>

### <span data-ttu-id="28c28-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c28-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="28c28-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28c28-129">OUTPUTS</span></span>

### <span data-ttu-id="28c28-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="28c28-130">System.Object</span></span>

## <span data-ttu-id="28c28-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28c28-131">NOTES</span></span>

## <span data-ttu-id="28c28-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28c28-132">RELATED LINKS</span></span>

[<span data-ttu-id="28c28-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c28-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="28c28-134">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c28-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="28c28-135">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c28-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


