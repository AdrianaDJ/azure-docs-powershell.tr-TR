---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322194"
---
# <span data-ttu-id="41e4f-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="41e4f-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="41e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="41e4f-103">Doğrudan bağlantı bilgilerini ayarlar veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="41e4f-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="41e4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41e4f-104">SYNTAX</span></span>

### <span data-ttu-id="41e4f-105">Bant genişliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="41e4f-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e4f-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="41e4f-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e4f-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="41e4f-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e4f-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="41e4f-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e4f-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="41e4f-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41e4f-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="41e4f-110">DESCRIPTION</span></span>
<span data-ttu-id="41e4f-111">Update-Azeşleme ile birlikte kullanıldığında, bu bir bellek işlemidir ve yalnızca ile devam eder `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="41e4f-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="41e4f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41e4f-112">EXAMPLES</span></span>

### <span data-ttu-id="41e4f-113">Bant genişliğini yükseltme</span><span class="sxs-lookup"><span data-stu-id="41e4f-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="41e4f-114">Bellekteki eşleme nesnesindeki bant genişliğini yükseltir.</span><span class="sxs-lookup"><span data-stu-id="41e4f-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="41e4f-115">BGP oturum adresini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="41e4f-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="41e4f-116">Bellekteki eşleme nesnesindeki ilk bağlantının eşleme adresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="41e4f-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="41e4f-117">Eşleme hizmeti için güncelleştirme kullanımı</span><span class="sxs-lookup"><span data-stu-id="41e4f-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="41e4f-118">Bağlantıyı eşleme hizmeti ile kullanmak üzere güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="41e4f-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="41e4f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41e4f-119">PARAMETERS</span></span>

### <span data-ttu-id="41e4f-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="41e4f-120">-BandwidthInMbps</span></span>
<span data-ttu-id="41e4f-121">Bu konumda, Mbps cinsinden önerilen bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="41e4f-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e4f-122">-DefaultProfile</span></span>
<span data-ttu-id="41e4f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41e4f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e4f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41e4f-124">-InputObject</span></span>
<span data-ttu-id="41e4f-125">Doğrudan bağlantı nesnesi</span><span class="sxs-lookup"><span data-stu-id="41e4f-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="41e4f-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="41e4f-127">En yüksek tanıtılan IPv4</span><span class="sxs-lookup"><span data-stu-id="41e4f-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="41e4f-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="41e4f-129">En yüksek tanıtılan IPv6</span><span class="sxs-lookup"><span data-stu-id="41e4f-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="41e4f-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="41e4f-131">Oturum için MD5 kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="41e4f-131">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="41e4f-132">-SessionPrefixV4</span></span>
<span data-ttu-id="41e4f-133">Eş oturumu IPv4 adresi</span><span class="sxs-lookup"><span data-stu-id="41e4f-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="41e4f-134">-SessionPrefixV6</span></span>
<span data-ttu-id="41e4f-135">Eş oturumu IPv6 adresi</span><span class="sxs-lookup"><span data-stu-id="41e4f-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="41e4f-136">-UseForPeeringService</span></span>
<span data-ttu-id="41e4f-137">Microsoft eşleme hizmeti (MPS) ile kullanımı etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="41e4f-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e4f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e4f-138">CommonParameters</span></span>
<span data-ttu-id="41e4f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41e4f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e4f-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41e4f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e4f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41e4f-141">INPUTS</span></span>

### <span data-ttu-id="41e4f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDırectconnection</span><span class="sxs-lookup"><span data-stu-id="41e4f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="41e4f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41e4f-143">OUTPUTS</span></span>

### <span data-ttu-id="41e4f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDırectconnection</span><span class="sxs-lookup"><span data-stu-id="41e4f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="41e4f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41e4f-145">NOTES</span></span>

## <span data-ttu-id="41e4f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41e4f-146">RELATED LINKS</span></span>
