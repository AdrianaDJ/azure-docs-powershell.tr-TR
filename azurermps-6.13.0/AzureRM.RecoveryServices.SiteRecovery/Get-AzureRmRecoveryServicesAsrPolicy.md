---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: aeceb76fe2f1faf6e7e1f2ddf09ee9262370e8ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591915"
---
# <span data-ttu-id="23a1d-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="23a1d-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="23a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="23a1d-103">ASR çoğaltma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="23a1d-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23a1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23a1d-104">SYNTAX</span></span>

### <span data-ttu-id="23a1d-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23a1d-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23a1d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="23a1d-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23a1d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="23a1d-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23a1d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="23a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="23a1d-109">**Get-AzureRmRecoveryServicesAsrPolicy** cmdlet 'i, yapılandırılmış Azure Site Recovery çoğaltma ilkelerinin listesini veya ad ile belirli bir çoğaltma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="23a1d-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="23a1d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23a1d-110">EXAMPLES</span></span>

### <span data-ttu-id="23a1d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23a1d-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="23a1d-112">Çoğaltma ilkeleri listesi</span><span class="sxs-lookup"><span data-stu-id="23a1d-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="23a1d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="23a1d-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="23a1d-114">Adla yeniden Tuns çoğaltma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="23a1d-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="23a1d-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="23a1d-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="23a1d-116">Belirtilen kolay ada sahip çoğaltma ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="23a1d-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="23a1d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23a1d-117">PARAMETERS</span></span>

### <span data-ttu-id="23a1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a1d-118">-DefaultProfile</span></span>
<span data-ttu-id="23a1d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23a1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="23a1d-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="23a1d-120">-FriendlyName</span></span>
<span data-ttu-id="23a1d-121">ASR çoğaltma ilkesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23a1d-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="23a1d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="23a1d-122">-Name</span></span>
<span data-ttu-id="23a1d-123">ASR çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23a1d-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="23a1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a1d-124">CommonParameters</span></span>
<span data-ttu-id="23a1d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23a1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a1d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a1d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a1d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23a1d-127">INPUTS</span></span>

### <span data-ttu-id="23a1d-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23a1d-128">None</span></span>

## <span data-ttu-id="23a1d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23a1d-129">OUTPUTS</span></span>

### <span data-ttu-id="23a1d-130">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., 4.0.0.0 covery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version =, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="23a1d-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="23a1d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23a1d-131">NOTES</span></span>

## <span data-ttu-id="23a1d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23a1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="23a1d-133">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="23a1d-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="23a1d-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="23a1d-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
