---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 5862d76c574b469d3bc0e559892b505e1b90beab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588834"
---
# <span data-ttu-id="c9680-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c9680-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c9680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9680-102">SYNOPSIS</span></span>
<span data-ttu-id="c9680-103">Kurtarma Hizmetleri kasasındaki ASR koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c9680-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9680-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9680-104">SYNTAX</span></span>

### <span data-ttu-id="c9680-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9680-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9680-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c9680-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9680-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c9680-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9680-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9680-108">DESCRIPTION</span></span>
<span data-ttu-id="c9680-109">**Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet 'ı, kurtarma hizmetleri kasasındaki Azure Site Recovery koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c9680-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="c9680-110">Koruma kapsayıcısı, korunabilir (keşfedilen) ve sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="c9680-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="c9680-111">Çoğaltma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korunabilir öğeye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c9680-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="c9680-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9680-112">EXAMPLES</span></span>

### <span data-ttu-id="c9680-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9680-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="c9680-114">Fabric $fabric koruma kapsayıcısı listesi.</span><span class="sxs-lookup"><span data-stu-id="c9680-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="c9680-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c9680-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="c9680-116">Yapıda $fabric koruma kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c9680-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="c9680-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c9680-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="c9680-118">Doku kapsayıcısı kolay adla $fabric.</span><span class="sxs-lookup"><span data-stu-id="c9680-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="c9680-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9680-119">PARAMETERS</span></span>

### <span data-ttu-id="c9680-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9680-120">-DefaultProfile</span></span>
<span data-ttu-id="c9680-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9680-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c9680-122">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="c9680-122">-Fabric</span></span>
<span data-ttu-id="c9680-123">Belirtilen ASR dokusunda koruma kapsayıcısını arayın.</span><span class="sxs-lookup"><span data-stu-id="c9680-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9680-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c9680-124">-FriendlyName</span></span>
<span data-ttu-id="c9680-125">Arama yapılacak ASR koruma kapsayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9680-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c9680-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9680-126">-Name</span></span>
<span data-ttu-id="c9680-127">Bakılacak ASR koruma kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9680-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c9680-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9680-128">CommonParameters</span></span>
<span data-ttu-id="c9680-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9680-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9680-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9680-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9680-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9680-131">INPUTS</span></span>

### <span data-ttu-id="c9680-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c9680-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c9680-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9680-133">OUTPUTS</span></span>

### <span data-ttu-id="c9680-134">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Hizmetlerçok. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c9680-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c9680-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9680-135">NOTES</span></span>

## <span data-ttu-id="c9680-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9680-136">RELATED LINKS</span></span>
