---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 87d89766468008548db70c757ee173cd141dc946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933044"
---
# <span data-ttu-id="0f273-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0f273-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="0f273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f273-102">SYNOPSIS</span></span>
<span data-ttu-id="0f273-103">ASR çoğaltma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="0f273-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="0f273-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f273-104">SYNTAX</span></span>

### <span data-ttu-id="0f273-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f273-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f273-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0f273-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f273-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f273-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f273-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f273-108">DESCRIPTION</span></span>
<span data-ttu-id="0f273-109">**Get-AzRecoveryServicesAsrPolicy** cmdlet 'i, yapılandırılmış Azure Site Recovery çoğaltma ilkelerinin listesini veya ad ile belirli bir çoğaltma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="0f273-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="0f273-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f273-110">EXAMPLES</span></span>

### <span data-ttu-id="0f273-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f273-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="0f273-112">Çoğaltma ilkeleri listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="0f273-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="0f273-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0f273-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="0f273-114">Ada sahip çoğaltma ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f273-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="0f273-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0f273-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="0f273-116">Belirtilen kolay ada sahip çoğaltma ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f273-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="0f273-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f273-117">PARAMETERS</span></span>

### <span data-ttu-id="0f273-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f273-118">-DefaultProfile</span></span>
<span data-ttu-id="0f273-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f273-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0f273-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f273-120">-FriendlyName</span></span>
<span data-ttu-id="0f273-121">ASR çoğaltma ilkesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f273-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="0f273-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f273-122">-Name</span></span>
<span data-ttu-id="0f273-123">ASR çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f273-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="0f273-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f273-124">CommonParameters</span></span>
<span data-ttu-id="0f273-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f273-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f273-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f273-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f273-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f273-127">INPUTS</span></span>

### <span data-ttu-id="0f273-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0f273-128">None</span></span>

## <span data-ttu-id="0f273-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f273-129">OUTPUTS</span></span>

### <span data-ttu-id="0f273-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="0f273-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="0f273-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f273-131">NOTES</span></span>

## <span data-ttu-id="0f273-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f273-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f273-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0f273-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="0f273-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0f273-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)