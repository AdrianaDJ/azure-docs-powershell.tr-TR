---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 33410022800111097610116732f6f137dfac41bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933422"
---
# <span data-ttu-id="9e231-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e231-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9e231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e231-102">SYNOPSIS</span></span>
<span data-ttu-id="9e231-103">Bir Azure Site kurtarma planının içeriğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9e231-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="9e231-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e231-104">SYNTAX</span></span>

### <span data-ttu-id="9e231-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e231-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e231-106">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="9e231-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e231-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e231-107">DESCRIPTION</span></span>
<span data-ttu-id="9e231-108">**Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'i, belirtilen ASR kurtarma planı NESNESININ veya ASR kurtarma planı tanımı JSON dosyasının içeriğini kullanarak kurtarma planının içeriğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9e231-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="9e231-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e231-109">EXAMPLES</span></span>

### <span data-ttu-id="9e231-110">Örnek 1: kurtarma planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9e231-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="9e231-111">Belirtilen ASR kurtarma planı nesnesinin içeriğini kullanarak kurtarma planı güncelleştirme işlemini başlatın ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e231-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9e231-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e231-112">PARAMETERS</span></span>

### <span data-ttu-id="9e231-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e231-113">-DefaultProfile</span></span>
<span data-ttu-id="9e231-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e231-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e231-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e231-115">-InputObject</span></span>
<span data-ttu-id="9e231-116">Cmdlet 'e giriş nesnesi: nesne tarafından başvurulan kurtarma planını güncelleştirmek için kullanılan ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e231-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e231-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="9e231-117">-Path</span></span>
<span data-ttu-id="9e231-118">Kurtarma planını güncelleştirmek için kullanılan kurtarma planı tanımı JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e231-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e231-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e231-119">-Confirm</span></span>
<span data-ttu-id="9e231-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e231-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e231-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e231-121">-WhatIf</span></span>
<span data-ttu-id="9e231-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e231-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e231-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e231-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e231-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e231-124">CommonParameters</span></span>
<span data-ttu-id="9e231-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e231-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e231-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e231-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e231-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e231-127">INPUTS</span></span>

### <span data-ttu-id="9e231-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e231-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9e231-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e231-129">OUTPUTS</span></span>

### <span data-ttu-id="9e231-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9e231-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9e231-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e231-131">NOTES</span></span>

## <span data-ttu-id="9e231-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e231-132">RELATED LINKS</span></span>

[<span data-ttu-id="9e231-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e231-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9e231-134">Yeni-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e231-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9e231-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e231-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)