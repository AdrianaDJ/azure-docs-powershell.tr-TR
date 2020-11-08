---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268412"
---
# <span data-ttu-id="87d76-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="87d76-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="87d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87d76-102">SYNOPSIS</span></span>
<span data-ttu-id="87d76-103">Bir eşleme oluşturmak veya değiştirmek için kullanılacak bellek PSObject öğesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87d76-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="87d76-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87d76-104">SYNTAX</span></span>

### <span data-ttu-id="87d76-105">IPv4Address (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87d76-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87d76-106">IPv6Adresi</span><span class="sxs-lookup"><span data-stu-id="87d76-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87d76-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="87d76-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87d76-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="87d76-108">DESCRIPTION</span></span>
<span data-ttu-id="87d76-109">Bellekte bir PSObject oluşturur</span><span class="sxs-lookup"><span data-stu-id="87d76-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="87d76-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87d76-110">EXAMPLES</span></span>

### <span data-ttu-id="87d76-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="87d76-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="87d76-112">Yerel bağlantı nesnesi</span><span class="sxs-lookup"><span data-stu-id="87d76-112">Local connection object</span></span>

## <span data-ttu-id="87d76-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87d76-113">PARAMETERS</span></span>

### <span data-ttu-id="87d76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d76-114">-DefaultProfile</span></span>
<span data-ttu-id="87d76-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87d76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d76-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="87d76-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="87d76-117">En yüksek tanıtılan IPv4</span><span class="sxs-lookup"><span data-stu-id="87d76-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d76-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="87d76-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="87d76-119">En yüksek tanıtılan IPv6</span><span class="sxs-lookup"><span data-stu-id="87d76-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d76-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="87d76-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="87d76-121">Oturum için MD5 kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="87d76-121">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d76-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="87d76-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="87d76-123">Bulunan eşleme olanağı kimliği https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="87d76-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="87d76-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="87d76-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="87d76-125">Eş oturumu IPv4 adresi</span><span class="sxs-lookup"><span data-stu-id="87d76-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d76-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="87d76-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="87d76-127">Eş oturumu IPv6 adresi</span><span class="sxs-lookup"><span data-stu-id="87d76-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d76-128">CommonParameters</span></span>
<span data-ttu-id="87d76-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87d76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d76-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="87d76-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d76-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87d76-131">INPUTS</span></span>

### <span data-ttu-id="87d76-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="87d76-132">None</span></span>

## <span data-ttu-id="87d76-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87d76-133">OUTPUTS</span></span>

### <span data-ttu-id="87d76-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d76-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="87d76-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87d76-135">NOTES</span></span>

## <span data-ttu-id="87d76-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87d76-136">RELATED LINKS</span></span>
