---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594594"
---
# <span data-ttu-id="d8a51-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8a51-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d8a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a51-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a51-103">Azure Site Recovery çoğaltma korumalı öğelerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a51-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8a51-104">SYNTAX</span></span>

### <span data-ttu-id="d8a51-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8a51-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="d8a51-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d8a51-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="d8a51-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8a51-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="d8a51-108">Bykorunabilir ıtemobject</span><span class="sxs-lookup"><span data-stu-id="d8a51-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="d8a51-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8a51-109">DESCRIPTION</span></span>
<span data-ttu-id="d8a51-110">**Get-Azurermrecoveryservicesasrreplicationkorunabilir koruyucudıtem** cmdlet 'i, belirtilen ASR koruma kapsayıcısından, belirtilen ASR çoğaltması korumalı öğesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a51-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="d8a51-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8a51-111">EXAMPLES</span></span>

### <span data-ttu-id="d8a51-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8a51-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="d8a51-113">Belirtilen ASR koruma kapsayıcısındaki tüm çoğaltma korumalı öğeleri listeler.</span><span class="sxs-lookup"><span data-stu-id="d8a51-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="d8a51-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8a51-114">PARAMETERS</span></span>

### <span data-ttu-id="d8a51-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8a51-115">-FriendlyName</span></span>
<span data-ttu-id="d8a51-116">Alınacak çoğaltma korumalı öğenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-116">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="d8a51-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8a51-117">-Name</span></span>
<span data-ttu-id="d8a51-118">Alınacak çoğaltma korumalı öğenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-118">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="d8a51-119">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="d8a51-119">-ProtectableItem</span></span>
<span data-ttu-id="d8a51-120">ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="d8a51-121">Cmdlet, öğe korumalıysa belirtilen ASR korumalı tablo öğesine karşılık gelen ASR çoğaltması korumalı öğesini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a51-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a51-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d8a51-122">-ProtectionContainer</span></span>
<span data-ttu-id="d8a51-123">Çoğaltma korumalı öğesine karşılık gelen ASR koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a51-124">CommonParameters</span></span>
<span data-ttu-id="d8a51-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8a51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a51-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a51-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a51-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8a51-127">INPUTS</span></span>

### <span data-ttu-id="d8a51-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d8a51-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="d8a51-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="d8a51-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d8a51-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8a51-130">OUTPUTS</span></span>

### <span data-ttu-id="d8a51-131">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir (4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8a51-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8a51-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8a51-132">NOTES</span></span>

## <span data-ttu-id="d8a51-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8a51-133">RELATED LINKS</span></span>

[<span data-ttu-id="d8a51-134">New-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d8a51-135">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d8a51-136">Set-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="d8a51-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
