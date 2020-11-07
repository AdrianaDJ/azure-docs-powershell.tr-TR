---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 6dd1c87617d83754af430ae25aea1b47aaaa34e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759581"
---
# <span data-ttu-id="a8b7c-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="a8b7c-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="a8b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b7c-103">Korumalı makinelere Mobility Service Agent güncelleştirmelerini itme.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="a8b7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8b7c-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="a8b7c-106">**Update-Azrecoveryservicesasrsoityservice** cmdlet 'i korumalı makinelere Mobility hizmet Aracısı güncelleştirmelerini itme girişiminde bulunur (güncelleştirme varsa).</span><span class="sxs-lookup"><span data-stu-id="a8b7c-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="a8b7c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8b7c-107">EXAMPLES</span></span>

### <span data-ttu-id="a8b7c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8b7c-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="a8b7c-109">Güncelleştirme çoğaltması korumalı öğenin Sloglık hizmet aracısının izlenmesi işi.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="a8b7c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8b7c-110">PARAMETERS</span></span>

### <span data-ttu-id="a8b7c-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a8b7c-111">-Account</span></span>
<span data-ttu-id="a8b7c-112">Güncelleştirmeyi göndermek için kullanılacak farklı hesapla hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="a8b7c-113">Makine güncellenecek olan ASR dokuda farklı bir Run as hesabı listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b7c-114">-DefaultProfile</span></span>
<span data-ttu-id="a8b7c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8b7c-116">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a8b7c-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a8b7c-117">Güncelleştirilecek Azure Site Recovery çoğaltma korumalı öğesi.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8b7c-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8b7c-118">-Confirm</span></span>
<span data-ttu-id="a8b7c-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b7c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b7c-120">-WhatIf</span></span>
<span data-ttu-id="a8b7c-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8b7c-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b7c-123">CommonParameters</span></span>
<span data-ttu-id="a8b7c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b7c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b7c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b7c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8b7c-126">INPUTS</span></span>

### <span data-ttu-id="a8b7c-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a8b7c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a8b7c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8b7c-128">OUTPUTS</span></span>

### <span data-ttu-id="a8b7c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a8b7c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a8b7c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8b7c-130">NOTES</span></span>

## <span data-ttu-id="a8b7c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8b7c-131">RELATED LINKS</span></span>