---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 876d30cd3c046136acc24a8492425c69fc845f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588837"
---
# <span data-ttu-id="95def-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="95def-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="95def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95def-102">SYNOPSIS</span></span>
<span data-ttu-id="95def-103">Bir ASR koruma kapsayıcısındaki korunabilir öğeleri edinin.</span><span class="sxs-lookup"><span data-stu-id="95def-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95def-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95def-104">SYNTAX</span></span>

### <span data-ttu-id="95def-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95def-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95def-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="95def-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95def-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="95def-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95def-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95def-108">DESCRIPTION</span></span>
<span data-ttu-id="95def-109">**Get-Azurermrecoveryservicesasrkorunabilir TableItem** cmdlet 'i, bir Azure Site Recovery koruma kapsayıcısındaki korunabilir öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="95def-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="95def-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95def-110">EXAMPLES</span></span>

### <span data-ttu-id="95def-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95def-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="95def-112">Belirtilen ASR koruma kapsayıcısındaki korunabilir tüm öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="95def-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="95def-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="95def-113">Example 2</span></span>
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

<span data-ttu-id="95def-114">Belirtilen ASR koruma kapsayıcısındaki korunabilir öğeleri ve verilen kolay adı alın.</span><span class="sxs-lookup"><span data-stu-id="95def-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="95def-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="95def-115">Example 3</span></span>
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

<span data-ttu-id="95def-116">Belirtilen ASR koruma kapsayıcısındaki korunabilir tüm öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="95def-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="95def-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95def-117">PARAMETERS</span></span>

### <span data-ttu-id="95def-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95def-118">-DefaultProfile</span></span>
<span data-ttu-id="95def-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95def-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95def-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="95def-120">-FriendlyName</span></span>
<span data-ttu-id="95def-121">ASR korunabilir öğesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95def-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95def-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="95def-122">-Name</span></span>
<span data-ttu-id="95def-123">ASR korunabilir öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95def-123">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95def-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="95def-124">-ProtectionContainer</span></span>
<span data-ttu-id="95def-125">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95def-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95def-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95def-126">CommonParameters</span></span>
<span data-ttu-id="95def-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95def-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95def-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95def-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95def-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95def-129">INPUTS</span></span>

### <span data-ttu-id="95def-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="95def-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="95def-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95def-131">OUTPUTS</span></span>

### <span data-ttu-id="95def-132">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. Asrkorunabilir öğe, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="95def-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="95def-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95def-133">NOTES</span></span>

## <span data-ttu-id="95def-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95def-134">RELATED LINKS</span></span>

[<span data-ttu-id="95def-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="95def-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="95def-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="95def-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
