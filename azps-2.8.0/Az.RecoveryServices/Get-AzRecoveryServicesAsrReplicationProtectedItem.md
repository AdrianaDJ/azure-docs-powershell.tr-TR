---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933030"
---
# <span data-ttu-id="709bf-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="709bf-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="709bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709bf-102">SYNOPSIS</span></span>
<span data-ttu-id="709bf-103">Azure Site Recovery çoğaltma korumalı öğelerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="709bf-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="709bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="709bf-104">SYNTAX</span></span>

### <span data-ttu-id="709bf-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="709bf-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709bf-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="709bf-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709bf-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="709bf-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709bf-108">Bykorunabilir ıtemobject</span><span class="sxs-lookup"><span data-stu-id="709bf-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="709bf-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="709bf-109">DESCRIPTION</span></span>
<span data-ttu-id="709bf-110">**Get-Azrecoveryservicesasrreplicationkorutdıtem** cmdlet 'i, belirtilen ASR koruma kapsayıcısından, belirtilen ASR çoğaltması korumalı öğesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="709bf-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="709bf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="709bf-111">EXAMPLES</span></span>

### <span data-ttu-id="709bf-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="709bf-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="709bf-113">Belirtilen ASR koruma kapsayıcısındaki tüm çoğaltma korumalı öğeleri listeler.</span><span class="sxs-lookup"><span data-stu-id="709bf-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="709bf-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="709bf-114">PARAMETERS</span></span>

### <span data-ttu-id="709bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709bf-115">-DefaultProfile</span></span>
<span data-ttu-id="709bf-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="709bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="709bf-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="709bf-117">-FriendlyName</span></span>
<span data-ttu-id="709bf-118">Alınacak çoğaltma korumalı öğenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709bf-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="709bf-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="709bf-119">-Name</span></span>
<span data-ttu-id="709bf-120">Alınacak çoğaltma korumalı öğenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709bf-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="709bf-121">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="709bf-121">-ProtectableItem</span></span>
<span data-ttu-id="709bf-122">ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="709bf-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="709bf-123">Cmdlet, öğe korumalıysa belirtilen ASR korumalı tablo öğesine karşılık gelen ASR çoğaltması korumalı öğesini alır.</span><span class="sxs-lookup"><span data-stu-id="709bf-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="709bf-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="709bf-124">-ProtectionContainer</span></span>
<span data-ttu-id="709bf-125">Çoğaltma korumalı öğesine karşılık gelen ASR koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="709bf-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="709bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709bf-126">CommonParameters</span></span>
<span data-ttu-id="709bf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="709bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709bf-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="709bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709bf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="709bf-129">INPUTS</span></span>

### <span data-ttu-id="709bf-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="709bf-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="709bf-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="709bf-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="709bf-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="709bf-132">OUTPUTS</span></span>

### <span data-ttu-id="709bf-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="709bf-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="709bf-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="709bf-134">NOTES</span></span>

## <span data-ttu-id="709bf-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="709bf-135">RELATED LINKS</span></span>

[<span data-ttu-id="709bf-136">New-Azrecoveryservicesasrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="709bf-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="709bf-137">Remove-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="709bf-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="709bf-138">Set-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="709bf-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
