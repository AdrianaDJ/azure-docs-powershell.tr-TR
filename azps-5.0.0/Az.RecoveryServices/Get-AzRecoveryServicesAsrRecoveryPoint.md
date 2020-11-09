---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325087"
---
# <span data-ttu-id="a00ec-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a00ec-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="a00ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a00ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a00ec-103">Bir çoğaltma korumalı öğesi için kullanılabilir kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="a00ec-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="a00ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a00ec-104">SYNTAX</span></span>

### <span data-ttu-id="a00ec-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a00ec-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a00ec-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a00ec-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a00ec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a00ec-107">DESCRIPTION</span></span>
<span data-ttu-id="a00ec-108">**Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet 'i çoğaltma korumalı bir öğe için kullanılabilir kurtarma noktalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a00ec-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="a00ec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a00ec-109">EXAMPLES</span></span>

### <span data-ttu-id="a00ec-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a00ec-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="a00ec-111">Belirtilen ASR çoğaltması korumalı öğesi için kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="a00ec-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="a00ec-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a00ec-112">PARAMETERS</span></span>

### <span data-ttu-id="a00ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00ec-113">-DefaultProfile</span></span>
<span data-ttu-id="a00ec-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a00ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a00ec-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a00ec-115">-Name</span></span>
<span data-ttu-id="a00ec-116">Alınacak kurtarma noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a00ec-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00ec-117">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a00ec-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a00ec-118">Kullanılabilir kurtarma noktaları listesinin alınacağı Azure Site Recovery çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a00ec-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="a00ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00ec-119">CommonParameters</span></span>
<span data-ttu-id="a00ec-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a00ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00ec-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a00ec-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00ec-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a00ec-122">INPUTS</span></span>

### <span data-ttu-id="a00ec-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a00ec-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a00ec-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a00ec-124">OUTPUTS</span></span>

### <span data-ttu-id="a00ec-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a00ec-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="a00ec-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a00ec-126">NOTES</span></span>

## <span data-ttu-id="a00ec-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a00ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="a00ec-128">Düzenle-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a00ec-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a00ec-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a00ec-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a00ec-130">Yeni-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a00ec-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a00ec-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a00ec-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a00ec-132">Güncelleştirme-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a00ec-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
