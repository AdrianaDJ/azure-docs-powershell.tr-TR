---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763643"
---
# <span data-ttu-id="2c5a9-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2c5a9-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2c5a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5a9-103">Bir Azure Site kurtarma planının içeriğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c5a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c5a9-104">SYNTAX</span></span>

### <span data-ttu-id="2c5a9-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c5a9-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c5a9-106">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="2c5a9-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c5a9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c5a9-107">DESCRIPTION</span></span>
<span data-ttu-id="2c5a9-108">**Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen ASR kurtarma planı NESNESININ veya ASR kurtarma planı tanımı JSON dosyasının içeriğini kullanarak kurtarma planının içeriğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="2c5a9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c5a9-109">EXAMPLES</span></span>

### <span data-ttu-id="2c5a9-110">Örnek 1: kurtarma planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2c5a9-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="2c5a9-111">Belirtilen ASR kurtarma planı nesnesinin içeriğini kullanarak kurtarma planı güncelleştirme işlemini başlatın ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2c5a9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c5a9-112">PARAMETERS</span></span>

### <span data-ttu-id="2c5a9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c5a9-113">-InputObject</span></span>
<span data-ttu-id="2c5a9-114">Cmdlet 'e giriş nesnesi: nesne tarafından başvurulan kurtarma planını güncelleştirmek için kullanılan ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c5a9-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="2c5a9-115">-Path</span></span>
<span data-ttu-id="2c5a9-116">Kurtarma planını güncelleştirmek için kullanılan kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5a9-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c5a9-117">-Confirm</span></span>
<span data-ttu-id="2c5a9-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5a9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5a9-119">-WhatIf</span></span>
<span data-ttu-id="2c5a9-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c5a9-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5a9-122">CommonParameters</span></span>
<span data-ttu-id="2c5a9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c5a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5a9-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5a9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5a9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c5a9-125">INPUTS</span></span>

### <span data-ttu-id="2c5a9-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2c5a9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2c5a9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c5a9-127">OUTPUTS</span></span>

### <span data-ttu-id="2c5a9-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="2c5a9-128">System.Object</span></span>

## <span data-ttu-id="2c5a9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c5a9-129">NOTES</span></span>

## <span data-ttu-id="2c5a9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c5a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c5a9-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2c5a9-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2c5a9-132">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2c5a9-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2c5a9-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2c5a9-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)


