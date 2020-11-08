---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278043"
---
# <span data-ttu-id="7311e-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7311e-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7311e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7311e-102">SYNOPSIS</span></span>
<span data-ttu-id="7311e-103">Belirtilen ASR çoğaltma ilkesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="7311e-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="7311e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7311e-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7311e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7311e-105">DESCRIPTION</span></span>
<span data-ttu-id="7311e-106">**Remove-AzRecoveryServicesAsrPolicy** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen çoğaltma ilkesini sildi.</span><span class="sxs-lookup"><span data-stu-id="7311e-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="7311e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7311e-107">EXAMPLES</span></span>

### <span data-ttu-id="7311e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7311e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="7311e-109">Belirtilen çoğaltma ilkesini silme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7311e-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7311e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7311e-110">PARAMETERS</span></span>

### <span data-ttu-id="7311e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7311e-111">-DefaultProfile</span></span>
<span data-ttu-id="7311e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7311e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7311e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7311e-113">-InputObject</span></span>
<span data-ttu-id="7311e-114">Cmdlet 'e giriş nesnesi: silinecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7311e-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="7311e-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="7311e-115">-Confirm</span></span>
<span data-ttu-id="7311e-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7311e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7311e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7311e-117">-WhatIf</span></span>
<span data-ttu-id="7311e-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7311e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7311e-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7311e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7311e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7311e-120">CommonParameters</span></span>
<span data-ttu-id="7311e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7311e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7311e-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7311e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7311e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7311e-123">INPUTS</span></span>

### <span data-ttu-id="7311e-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="7311e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="7311e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7311e-125">OUTPUTS</span></span>

### <span data-ttu-id="7311e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7311e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7311e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7311e-127">NOTES</span></span>

## <span data-ttu-id="7311e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7311e-128">RELATED LINKS</span></span>

[<span data-ttu-id="7311e-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7311e-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7311e-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7311e-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
