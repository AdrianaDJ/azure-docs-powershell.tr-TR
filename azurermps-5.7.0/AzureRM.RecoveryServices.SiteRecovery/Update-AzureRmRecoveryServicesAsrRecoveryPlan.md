---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 0cabaee1c1d9dfc8a627160ac01adaca81fe65c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592425"
---
# <span data-ttu-id="6f5e4-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6f5e4-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6f5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5e4-103">Bir Azure Site kurtarma planının içeriğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f5e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f5e4-104">SYNTAX</span></span>

### <span data-ttu-id="6f5e4-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f5e4-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f5e4-106">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="6f5e4-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f5e4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f5e4-107">DESCRIPTION</span></span>
<span data-ttu-id="6f5e4-108">**Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen ASR kurtarma planı NESNESININ veya ASR kurtarma planı tanımı JSON dosyasının içeriğini kullanarak kurtarma planının içeriğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="6f5e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f5e4-109">EXAMPLES</span></span>

### <span data-ttu-id="6f5e4-110">Örnek 1: kurtarma planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6f5e4-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="6f5e4-111">Belirtilen ASR kurtarma planı nesnesinin içeriğini kullanarak kurtarma planı güncelleştirme işlemini başlatın ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6f5e4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f5e4-112">PARAMETERS</span></span>

### <span data-ttu-id="6f5e4-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f5e4-113">-Confirm</span></span>
<span data-ttu-id="6f5e4-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f5e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5e4-115">-DefaultProfile</span></span>
<span data-ttu-id="6f5e4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="6f5e4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f5e4-117">-InputObject</span></span>
<span data-ttu-id="6f5e4-118">Cmdlet 'e giriş nesnesi: nesne tarafından başvurulan kurtarma planını güncelleştirmek için kullanılan ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-118">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="6f5e4-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="6f5e4-119">-Path</span></span>
<span data-ttu-id="6f5e4-120">Kurtarma planını güncelleştirmek için kullanılan kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-120">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="6f5e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f5e4-121">-WhatIf</span></span>
<span data-ttu-id="6f5e4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f5e4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f5e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5e4-124">CommonParameters</span></span>
<span data-ttu-id="6f5e4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f5e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5e4-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5e4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5e4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f5e4-127">INPUTS</span></span>

### <span data-ttu-id="6f5e4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6f5e4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="6f5e4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f5e4-129">OUTPUTS</span></span>

### <span data-ttu-id="6f5e4-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="6f5e4-130">System.Object</span></span>

## <span data-ttu-id="6f5e4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f5e4-131">NOTES</span></span>

## <span data-ttu-id="6f5e4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f5e4-132">RELATED LINKS</span></span>

[<span data-ttu-id="6f5e4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6f5e4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6f5e4-134">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6f5e4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6f5e4-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6f5e4-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)
