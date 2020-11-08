---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096092"
---
# <span data-ttu-id="6b130-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6b130-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="6b130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b130-102">SYNOPSIS</span></span>
<span data-ttu-id="6b130-103">Kurtarma Hizmetleri kasasındaki ASR koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="6b130-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="6b130-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b130-104">SYNTAX</span></span>

### <span data-ttu-id="6b130-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b130-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b130-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6b130-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b130-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b130-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b130-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b130-108">DESCRIPTION</span></span>
<span data-ttu-id="6b130-109">**Get-AzRecoveryServicesAsrProtectionContainer** cmdlet 'ı, kurtarma hizmetleri kasasındaki Azure Site Recovery koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="6b130-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="6b130-110">Koruma kapsayıcısı, korunabilir (keşfedilen) ve sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="6b130-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="6b130-111">Çoğaltma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korunabilir öğeye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="6b130-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="6b130-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b130-112">EXAMPLES</span></span>

### <span data-ttu-id="6b130-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6b130-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="6b130-114">Fabric $fabric koruma kapsayıcısı listesi.</span><span class="sxs-lookup"><span data-stu-id="6b130-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="6b130-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6b130-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="6b130-116">Yapıda $fabric koruma kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b130-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="6b130-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6b130-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="6b130-118">Doku kapsayıcısı kolay adla $fabric.</span><span class="sxs-lookup"><span data-stu-id="6b130-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="6b130-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b130-119">PARAMETERS</span></span>

### <span data-ttu-id="6b130-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b130-120">-DefaultProfile</span></span>
<span data-ttu-id="6b130-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b130-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b130-122">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="6b130-122">-Fabric</span></span>
<span data-ttu-id="6b130-123">Belirtilen ASR dokusunda koruma kapsayıcısını arayın.</span><span class="sxs-lookup"><span data-stu-id="6b130-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b130-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b130-124">-FriendlyName</span></span>
<span data-ttu-id="6b130-125">Arama yapılacak ASR koruma kapsayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b130-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="6b130-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b130-126">-Name</span></span>
<span data-ttu-id="6b130-127">Bakılacak ASR koruma kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b130-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="6b130-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b130-128">CommonParameters</span></span>
<span data-ttu-id="6b130-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b130-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b130-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b130-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b130-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b130-131">INPUTS</span></span>

### <span data-ttu-id="6b130-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6b130-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6b130-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b130-133">OUTPUTS</span></span>

### <span data-ttu-id="6b130-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6b130-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="6b130-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b130-135">NOTES</span></span>

## <span data-ttu-id="6b130-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b130-136">RELATED LINKS</span></span>
