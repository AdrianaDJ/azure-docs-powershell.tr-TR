---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266954"
---
# <span data-ttu-id="53bba-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="53bba-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="53bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bba-102">SYNOPSIS</span></span>
<span data-ttu-id="53bba-103">Bir ASR koruma kapsayıcısındaki korunabilir öğeleri edinin.</span><span class="sxs-lookup"><span data-stu-id="53bba-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="53bba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53bba-104">SYNTAX</span></span>

### <span data-ttu-id="53bba-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53bba-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bba-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="53bba-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bba-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="53bba-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bba-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="53bba-108">DESCRIPTION</span></span>
<span data-ttu-id="53bba-109">**Get-Azrecoveryservicesasrkorunabilir TableItem** cmdlet 'i, bir Azure Site Recovery koruma kapsayıcısındaki korunabilir öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="53bba-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="53bba-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53bba-110">EXAMPLES</span></span>

### <span data-ttu-id="53bba-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53bba-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="53bba-112">Belirtilen ASR koruma kapsayıcısındaki korunabilir tüm öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="53bba-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="53bba-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="53bba-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="53bba-114">Belirtilen ASR koruma kapsayıcısındaki korunabilir öğeleri ve verilen kolay adı alın.</span><span class="sxs-lookup"><span data-stu-id="53bba-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="53bba-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="53bba-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="53bba-116">Belirtilen ASR koruma kapsayıcısındaki korunabilir tüm öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="53bba-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="53bba-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53bba-117">PARAMETERS</span></span>

### <span data-ttu-id="53bba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bba-118">-DefaultProfile</span></span>
<span data-ttu-id="53bba-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53bba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="53bba-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="53bba-120">-FriendlyName</span></span>
<span data-ttu-id="53bba-121">ASR korunabilir öğesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53bba-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bba-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="53bba-122">-Name</span></span>
<span data-ttu-id="53bba-123">ASR korunabilir öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53bba-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="53bba-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="53bba-124">-ProtectionContainer</span></span>
<span data-ttu-id="53bba-125">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="53bba-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53bba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bba-126">CommonParameters</span></span>
<span data-ttu-id="53bba-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53bba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bba-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="53bba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bba-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53bba-129">INPUTS</span></span>

### <span data-ttu-id="53bba-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="53bba-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="53bba-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53bba-131">OUTPUTS</span></span>

### <span data-ttu-id="53bba-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="53bba-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="53bba-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53bba-133">NOTES</span></span>

## <span data-ttu-id="53bba-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53bba-134">RELATED LINKS</span></span>

[<span data-ttu-id="53bba-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="53bba-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="53bba-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="53bba-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
