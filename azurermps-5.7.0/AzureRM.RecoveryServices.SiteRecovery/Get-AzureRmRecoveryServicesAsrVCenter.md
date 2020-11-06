---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 689f432f117e67a3770518a3b2e86f1678f3662b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591649"
---
# <span data-ttu-id="7dc5b-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="7dc5b-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="7dc5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc5b-103">ASR yapısı tarafından belirtilen yapılandırma sunucusundaki bulma için kaydettirilmiş vCenter sunucularının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7dc5b-104">SYNTAX</span></span>

### <span data-ttu-id="7dc5b-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7dc5b-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dc5b-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7dc5b-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dc5b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7dc5b-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc5b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7dc5b-108">DESCRIPTION</span></span>
<span data-ttu-id="7dc5b-109">**Get-AzureRmRecoveryServicesAsrvCenter** cmdlet 'ı, ASR yapısı tarafından belirtilen yapılandırma sunucusundaki bulma Için kaydettirilmiş vCenter sunucularıyla ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="7dc5b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7dc5b-110">EXAMPLES</span></span>

### <span data-ttu-id="7dc5b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7dc5b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="7dc5b-112">Azure Site Recovery vCenter 'yi doku adına ve vCenter adına göre alın.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="7dc5b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7dc5b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="7dc5b-114">Azure Site Recovery vCenter listesini doku adına göre edinin.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="7dc5b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7dc5b-115">PARAMETERS</span></span>

### <span data-ttu-id="7dc5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc5b-116">-DefaultProfile</span></span>
<span data-ttu-id="7dc5b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc5b-118">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="7dc5b-118">-Fabric</span></span>
<span data-ttu-id="7dc5b-119">Yapılandırma sunucusunu temsil eden ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc5b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7dc5b-120">-Name</span></span>
<span data-ttu-id="7dc5b-121">VCenter sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-121">Name of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc5b-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7dc5b-122">-ResourceId</span></span>
<span data-ttu-id="7dc5b-123">VCenter 'ın RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc5b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc5b-124">CommonParameters</span></span>
<span data-ttu-id="7dc5b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc5b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc5b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc5b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7dc5b-127">INPUTS</span></span>

### <span data-ttu-id="7dc5b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7dc5b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7dc5b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7dc5b-129">OUTPUTS</span></span>

### <span data-ttu-id="7dc5b-130">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRvCenter, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7dc5b-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7dc5b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7dc5b-131">NOTES</span></span>

## <span data-ttu-id="7dc5b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7dc5b-132">RELATED LINKS</span></span>
