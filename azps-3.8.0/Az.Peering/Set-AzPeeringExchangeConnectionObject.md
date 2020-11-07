---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c09ff4ad7762eafc18d7890f9611c9b989841c95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937888"
---
# <span data-ttu-id="16bf9-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="16bf9-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="16bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="16bf9-103">Exchange bağlantı bilgilerini ayarlar veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="16bf9-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="16bf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16bf9-104">SYNTAX</span></span>

### <span data-ttu-id="16bf9-105">IPv6Adresi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16bf9-105">IPv6Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16bf9-106">IPv4Address</span><span class="sxs-lookup"><span data-stu-id="16bf9-106">IPv4Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16bf9-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="16bf9-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16bf9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="16bf9-108">DESCRIPTION</span></span>
<span data-ttu-id="16bf9-109">Update-Azeşleme ile birlikte kullanıldığında, bu bir bellek işlemidir ve yalnızca ile devam eder `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="16bf9-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="16bf9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16bf9-110">EXAMPLES</span></span>

### <span data-ttu-id="16bf9-111">MD5 karma değerini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="16bf9-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="16bf9-112">Bellekteki eşleme nesnesindeki ilk bağlantının MD5 karmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="16bf9-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="16bf9-113">BGP oturum adresini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="16bf9-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="16bf9-114">Bellekteki eşleme nesnesindeki ilk bağlantının eşleme adresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="16bf9-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="16bf9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16bf9-115">PARAMETERS</span></span>

### <span data-ttu-id="16bf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bf9-116">-DefaultProfile</span></span>
<span data-ttu-id="16bf9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16bf9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16bf9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16bf9-118">-InputObject</span></span>
<span data-ttu-id="16bf9-119">Exchange bağlantı nesnesi</span><span class="sxs-lookup"><span data-stu-id="16bf9-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16bf9-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="16bf9-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="16bf9-121">En yüksek tanıtılan IPv4</span><span class="sxs-lookup"><span data-stu-id="16bf9-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bf9-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="16bf9-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="16bf9-123">En yüksek tanıtılan IPv6</span><span class="sxs-lookup"><span data-stu-id="16bf9-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bf9-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="16bf9-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="16bf9-125">Oturum için MD5 kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="16bf9-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="16bf9-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="16bf9-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="16bf9-127">Eş oturumu IPv4 adresi</span><span class="sxs-lookup"><span data-stu-id="16bf9-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bf9-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="16bf9-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="16bf9-129">Eş oturumu IPv6 adresi</span><span class="sxs-lookup"><span data-stu-id="16bf9-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bf9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bf9-130">CommonParameters</span></span>
<span data-ttu-id="16bf9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16bf9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bf9-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="16bf9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bf9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16bf9-133">INPUTS</span></span>

### <span data-ttu-id="16bf9-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16bf9-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="16bf9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16bf9-135">OUTPUTS</span></span>

### <span data-ttu-id="16bf9-136">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16bf9-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="16bf9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16bf9-137">NOTES</span></span>

## <span data-ttu-id="16bf9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16bf9-138">RELATED LINKS</span></span>
