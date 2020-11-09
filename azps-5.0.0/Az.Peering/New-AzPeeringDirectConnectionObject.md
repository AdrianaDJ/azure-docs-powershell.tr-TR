---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323131"
---
# <span data-ttu-id="94784-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="94784-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="94784-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94784-102">SYNOPSIS</span></span>
<span data-ttu-id="94784-103">Bir eşleme oluşturmak veya değiştirmek için kullanılacak bellek PSObject öğesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94784-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="94784-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94784-104">SYNTAX</span></span>

### <span data-ttu-id="94784-105">IPv4PrefixIPv6Prefix (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94784-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94784-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="94784-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94784-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94784-107">DESCRIPTION</span></span>
<span data-ttu-id="94784-108">Bellekte bir PSObject oluşturur</span><span class="sxs-lookup"><span data-stu-id="94784-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="94784-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94784-109">EXAMPLES</span></span>

### <span data-ttu-id="94784-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94784-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="94784-111">Yeni yerel bağlantı</span><span class="sxs-lookup"><span data-stu-id="94784-111">New local connection</span></span>

### <span data-ttu-id="94784-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="94784-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="94784-113">Eşleme hizmeti etkinleştirilmiş ve Microsoft tarafından sağlanan IP adresleriyle doğrudan eşleme bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="94784-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="94784-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="94784-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="94784-115">Eşleme hizmeti etkin ve eş sağlanan IP adresleri kullanımıyla doğrudan eşleme bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="94784-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="94784-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="94784-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="94784-117">BGP oturumu IP adresleri olmadan doğrudan eşleme bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="94784-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="94784-118">BGP oturumunun yapılandırılmadan önce eşin IP adreslerini ayarlamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="94784-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="94784-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94784-119">PARAMETERS</span></span>

### <span data-ttu-id="94784-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="94784-120">-BandwidthInMbps</span></span>
<span data-ttu-id="94784-121">Bu konumda, Mbps cinsinden önerilen bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="94784-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94784-122">-DefaultProfile</span></span>
<span data-ttu-id="94784-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94784-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94784-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="94784-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="94784-125">En yüksek tanıtılan IPv4</span><span class="sxs-lookup"><span data-stu-id="94784-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="94784-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="94784-127">En yüksek tanıtılan IPv6</span><span class="sxs-lookup"><span data-stu-id="94784-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="94784-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="94784-129">Oturum için MD5 kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="94784-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-130">-Microsoftprovidedıadaddress</span><span class="sxs-lookup"><span data-stu-id="94784-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="94784-131">Microsoft 'un BGP oturum adreslerini sağlamasını belirten bayrağı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="94784-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="94784-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="94784-133">Bulunan eşleme olanağı kimliği https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="94784-133">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="94784-134">-SessionPrefixV4</span></span>
<span data-ttu-id="94784-135">Eş oturumu IPv4 adresi</span><span class="sxs-lookup"><span data-stu-id="94784-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="94784-136">-SessionPrefixV6</span></span>
<span data-ttu-id="94784-137">Eş oturumu IPv6 adresi</span><span class="sxs-lookup"><span data-stu-id="94784-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="94784-138">-UseForPeeringService</span></span>
<span data-ttu-id="94784-139">Microsoft eşleme hizmeti (MPS) ile kullanımı etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="94784-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94784-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94784-140">CommonParameters</span></span>
<span data-ttu-id="94784-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94784-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94784-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94784-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94784-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94784-143">INPUTS</span></span>

### <span data-ttu-id="94784-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="94784-144">None</span></span>

## <span data-ttu-id="94784-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94784-145">OUTPUTS</span></span>

### <span data-ttu-id="94784-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDırectconnection</span><span class="sxs-lookup"><span data-stu-id="94784-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="94784-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94784-147">NOTES</span></span>

## <span data-ttu-id="94784-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94784-148">RELATED LINKS</span></span>
