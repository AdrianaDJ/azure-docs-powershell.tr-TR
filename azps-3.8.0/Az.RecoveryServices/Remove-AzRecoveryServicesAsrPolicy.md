---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098119"
---
# <span data-ttu-id="33fb8-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="33fb8-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="33fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="33fb8-103">Belirtilen ASR çoğaltma ilkesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="33fb8-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="33fb8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33fb8-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33fb8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="33fb8-106">**Remove-AzRecoveryServicesAsrPolicy** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen çoğaltma ilkesini sildi.</span><span class="sxs-lookup"><span data-stu-id="33fb8-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="33fb8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="33fb8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33fb8-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="33fb8-109">Belirtilen çoğaltma ilkesini silme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="33fb8-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="33fb8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="33fb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fb8-111">-DefaultProfile</span></span>
<span data-ttu-id="33fb8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33fb8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="33fb8-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33fb8-113">-InputObject</span></span>
<span data-ttu-id="33fb8-114">Cmdlet 'e giriş nesnesi: silinecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="33fb8-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33fb8-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="33fb8-115">-Confirm</span></span>
<span data-ttu-id="33fb8-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="33fb8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33fb8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33fb8-117">-WhatIf</span></span>
<span data-ttu-id="33fb8-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33fb8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33fb8-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33fb8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33fb8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fb8-120">CommonParameters</span></span>
<span data-ttu-id="33fb8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33fb8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fb8-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="33fb8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fb8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33fb8-123">INPUTS</span></span>

### <span data-ttu-id="33fb8-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="33fb8-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="33fb8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33fb8-125">OUTPUTS</span></span>

### <span data-ttu-id="33fb8-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="33fb8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="33fb8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33fb8-127">NOTES</span></span>

## <span data-ttu-id="33fb8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33fb8-128">RELATED LINKS</span></span>

[<span data-ttu-id="33fb8-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="33fb8-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="33fb8-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="33fb8-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
