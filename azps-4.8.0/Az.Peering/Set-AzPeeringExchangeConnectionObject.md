---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109400"
---
# <span data-ttu-id="d7e60-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="d7e60-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="d7e60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e60-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e60-103">Exchange bağlantı bilgilerini ayarlar veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7e60-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="d7e60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7e60-104">SYNTAX</span></span>

### <span data-ttu-id="d7e60-105">IPv4Address (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7e60-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e60-106">IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="d7e60-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e60-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="d7e60-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7e60-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7e60-108">DESCRIPTION</span></span>
<span data-ttu-id="d7e60-109">Update-Azeşleme ile birlikte kullanıldığında, bu bir bellek işlemidir ve yalnızca ile devam eder `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="d7e60-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="d7e60-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7e60-110">EXAMPLES</span></span>

### <span data-ttu-id="d7e60-111">MD5 karma değerini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d7e60-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="d7e60-112">Bellekteki eşleme nesnesindeki ilk bağlantının MD5 karmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7e60-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="d7e60-113">BGP oturum adresini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d7e60-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="d7e60-114">Bellekteki eşleme nesnesindeki ilk bağlantının eşleme adresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7e60-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="d7e60-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7e60-115">PARAMETERS</span></span>

### <span data-ttu-id="d7e60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e60-116">-DefaultProfile</span></span>
<span data-ttu-id="d7e60-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7e60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e60-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7e60-118">-InputObject</span></span>
<span data-ttu-id="d7e60-119">Exchange bağlantı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d7e60-119">The exchange connection object</span></span>

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

### <span data-ttu-id="d7e60-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="d7e60-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="d7e60-121">En yüksek tanıtılan IPv4</span><span class="sxs-lookup"><span data-stu-id="d7e60-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="d7e60-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="d7e60-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="d7e60-123">En yüksek tanıtılan IPv6</span><span class="sxs-lookup"><span data-stu-id="d7e60-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="d7e60-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="d7e60-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="d7e60-125">Oturum için MD5 kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="d7e60-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="d7e60-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="d7e60-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="d7e60-127">Eş oturumu IPv4 adresi</span><span class="sxs-lookup"><span data-stu-id="d7e60-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="d7e60-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="d7e60-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="d7e60-129">Eş oturumu IPv6 adresi</span><span class="sxs-lookup"><span data-stu-id="d7e60-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="d7e60-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e60-130">CommonParameters</span></span>
<span data-ttu-id="d7e60-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7e60-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e60-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7e60-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e60-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7e60-133">INPUTS</span></span>

### <span data-ttu-id="d7e60-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e60-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="d7e60-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7e60-135">OUTPUTS</span></span>

### <span data-ttu-id="d7e60-136">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e60-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="d7e60-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7e60-137">NOTES</span></span>

## <span data-ttu-id="d7e60-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7e60-138">RELATED LINKS</span></span>
