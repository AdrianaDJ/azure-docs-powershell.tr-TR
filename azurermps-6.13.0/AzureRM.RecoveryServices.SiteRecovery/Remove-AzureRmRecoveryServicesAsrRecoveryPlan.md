---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762104"
---
# <span data-ttu-id="f7f52-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7f52-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f7f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f52-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f52-103">Belirtilen ASR kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="f7f52-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7f52-104">SYNTAX</span></span>

### <span data-ttu-id="f7f52-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7f52-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f52-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f7f52-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f52-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7f52-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f52-108">**Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen kurtarma planını kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="f7f52-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="f7f52-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7f52-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f52-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f7f52-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="f7f52-111">Belirtilen kurtarma planının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f7f52-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f7f52-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7f52-112">PARAMETERS</span></span>

### <span data-ttu-id="f7f52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f52-113">-DefaultProfile</span></span>
<span data-ttu-id="f7f52-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7f52-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f7f52-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f52-115">-InputObject</span></span>
<span data-ttu-id="f7f52-116">Cmdlet 'e giriş nesnesi: kurtarma planına karşılık gelen ASR kurtarma planı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f7f52-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f52-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7f52-117">-Name</span></span>
<span data-ttu-id="f7f52-118">Silinecek kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f52-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="f7f52-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7f52-119">-Confirm</span></span>
<span data-ttu-id="f7f52-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7f52-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f52-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f52-121">-WhatIf</span></span>
<span data-ttu-id="f7f52-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7f52-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7f52-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7f52-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f52-124">CommonParameters</span></span>
<span data-ttu-id="f7f52-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7f52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f52-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f52-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7f52-127">INPUTS</span></span>

### <span data-ttu-id="f7f52-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7f52-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f7f52-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7f52-129">OUTPUTS</span></span>

### <span data-ttu-id="f7f52-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7f52-130">System.Object</span></span>

## <span data-ttu-id="f7f52-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7f52-131">NOTES</span></span>

## <span data-ttu-id="f7f52-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7f52-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7f52-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7f52-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f7f52-134">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7f52-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f7f52-135">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7f52-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


