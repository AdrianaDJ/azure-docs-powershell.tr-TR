---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5ccc65973d3dd6f86d3a2e88ba2494fd75df6e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588400"
---
# <span data-ttu-id="b4166-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b4166-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="b4166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4166-102">SYNOPSIS</span></span>
<span data-ttu-id="b4166-103">Azure Site Recovery çoğaltma korumalı öğelerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b4166-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4166-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4166-104">SYNTAX</span></span>

### <span data-ttu-id="b4166-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4166-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4166-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b4166-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4166-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b4166-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4166-108">Bykorunabilir ıtemobject</span><span class="sxs-lookup"><span data-stu-id="b4166-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4166-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4166-109">DESCRIPTION</span></span>
<span data-ttu-id="b4166-110">**Get-Azurermrecoveryservicesasrreplicationkorunabilir koruyucudıtem** cmdlet 'i, belirtilen ASR koruma kapsayıcısından, belirtilen ASR çoğaltması korumalı öğesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b4166-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="b4166-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4166-111">EXAMPLES</span></span>

### <span data-ttu-id="b4166-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4166-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="b4166-113">Belirtilen ASR koruma kapsayıcısındaki tüm çoğaltma korumalı öğeleri listeler.</span><span class="sxs-lookup"><span data-stu-id="b4166-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="b4166-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4166-114">PARAMETERS</span></span>

### <span data-ttu-id="b4166-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4166-115">-DefaultProfile</span></span>
<span data-ttu-id="b4166-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4166-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b4166-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b4166-117">-FriendlyName</span></span>
<span data-ttu-id="b4166-118">Alınacak çoğaltma korumalı öğenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4166-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="b4166-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4166-119">-Name</span></span>
<span data-ttu-id="b4166-120">Alınacak çoğaltma korumalı öğenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4166-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="b4166-121">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="b4166-121">-ProtectableItem</span></span>
<span data-ttu-id="b4166-122">ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4166-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="b4166-123">Cmdlet, öğe korumalıysa belirtilen ASR korumalı tablo öğesine karşılık gelen ASR çoğaltması korumalı öğesini alır.</span><span class="sxs-lookup"><span data-stu-id="b4166-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="b4166-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b4166-124">-ProtectionContainer</span></span>
<span data-ttu-id="b4166-125">Çoğaltma korumalı öğesine karşılık gelen ASR koruma kapsayıcısının ASR koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4166-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="b4166-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4166-126">CommonParameters</span></span>
<span data-ttu-id="b4166-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4166-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4166-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4166-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4166-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4166-129">INPUTS</span></span>

### <span data-ttu-id="b4166-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b4166-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="b4166-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="b4166-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="b4166-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4166-132">OUTPUTS</span></span>

### <span data-ttu-id="b4166-133">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir (4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b4166-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b4166-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4166-134">NOTES</span></span>

## <span data-ttu-id="b4166-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4166-135">RELATED LINKS</span></span>

[<span data-ttu-id="b4166-136">New-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="b4166-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b4166-137">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="b4166-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b4166-138">Set-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="b4166-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
