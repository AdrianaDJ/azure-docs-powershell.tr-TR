---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588402"
---
# <span data-ttu-id="4b36a-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4b36a-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="4b36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b36a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b36a-103">Bir çoğaltma korumalı öğesi için kullanılabilir kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b36a-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b36a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b36a-104">SYNTAX</span></span>

### <span data-ttu-id="4b36a-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b36a-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b36a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4b36a-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b36a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b36a-107">DESCRIPTION</span></span>
<span data-ttu-id="4b36a-108">**Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet 'i çoğaltma korumalı bir öğe için kullanılabilir kurtarma noktalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4b36a-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="4b36a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b36a-109">EXAMPLES</span></span>

### <span data-ttu-id="4b36a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b36a-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="4b36a-111">Belirtilen ASR çoğaltması korumalı öğesi için kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b36a-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="4b36a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b36a-112">PARAMETERS</span></span>

### <span data-ttu-id="4b36a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b36a-113">-DefaultProfile</span></span>
<span data-ttu-id="4b36a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b36a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4b36a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b36a-115">-Name</span></span>
<span data-ttu-id="4b36a-116">Alınacak kurtarma noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b36a-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="4b36a-117">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="4b36a-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4b36a-118">Kullanılabilir kurtarma noktaları listesinin alınacağı Azure Site Recovery çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b36a-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="4b36a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b36a-119">CommonParameters</span></span>
<span data-ttu-id="4b36a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b36a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b36a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b36a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b36a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b36a-122">INPUTS</span></span>

### <span data-ttu-id="4b36a-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="4b36a-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4b36a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b36a-124">OUTPUTS</span></span>

### <span data-ttu-id="4b36a-125">System. topluluklar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Services. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4b36a-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4b36a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b36a-126">NOTES</span></span>

## <span data-ttu-id="4b36a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b36a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b36a-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b36a-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4b36a-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b36a-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4b36a-130">Yeni-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b36a-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4b36a-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b36a-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4b36a-132">Güncelleştirme-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b36a-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
