---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a25375a565db8d2c69a423aa95033033de3f0f8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759737"
---
# <span data-ttu-id="c8157-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c8157-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="c8157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8157-102">SYNOPSIS</span></span>
<span data-ttu-id="c8157-103">ASR çoğaltma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c8157-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="c8157-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8157-104">SYNTAX</span></span>

### <span data-ttu-id="c8157-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8157-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8157-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c8157-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8157-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c8157-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8157-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8157-108">DESCRIPTION</span></span>
<span data-ttu-id="c8157-109">**Get-AzRecoveryServicesAsrPolicy** cmdlet 'i, yapılandırılmış Azure Site Recovery çoğaltma ilkelerinin listesini veya ad ile belirli bir çoğaltma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c8157-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="c8157-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8157-110">EXAMPLES</span></span>

### <span data-ttu-id="c8157-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c8157-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="c8157-112">Çoğaltma ilkeleri listesi</span><span class="sxs-lookup"><span data-stu-id="c8157-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="c8157-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c8157-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="c8157-114">Adla yeniden Tuns çoğaltma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="c8157-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="c8157-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c8157-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="c8157-116">Belirtilen kolay ada sahip çoğaltma ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c8157-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="c8157-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8157-117">PARAMETERS</span></span>

### <span data-ttu-id="c8157-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8157-118">-DefaultProfile</span></span>
<span data-ttu-id="c8157-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8157-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c8157-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c8157-120">-FriendlyName</span></span>
<span data-ttu-id="c8157-121">ASR çoğaltma ilkesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8157-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8157-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8157-122">-Name</span></span>
<span data-ttu-id="c8157-123">ASR çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8157-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="c8157-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8157-124">CommonParameters</span></span>
<span data-ttu-id="c8157-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8157-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8157-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8157-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8157-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8157-127">INPUTS</span></span>

### <span data-ttu-id="c8157-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c8157-128">None</span></span>

## <span data-ttu-id="c8157-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8157-129">OUTPUTS</span></span>

### <span data-ttu-id="c8157-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="c8157-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="c8157-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8157-131">NOTES</span></span>

## <span data-ttu-id="c8157-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8157-132">RELATED LINKS</span></span>

[<span data-ttu-id="c8157-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c8157-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="c8157-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c8157-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
