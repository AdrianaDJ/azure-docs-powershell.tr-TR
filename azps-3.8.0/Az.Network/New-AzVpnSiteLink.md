---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096493"
---
# <span data-ttu-id="b8a0c-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b8a0c-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="b8a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a0c-103">Azure Vpnsite nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b8a0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8a0c-104">SYNTAX</span></span>

### <span data-ttu-id="b8a0c-105">Byvpnsitelinkıpaddress</span><span class="sxs-lookup"><span data-stu-id="b8a0c-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8a0c-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="b8a0c-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8a0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8a0c-107">DESCRIPTION</span></span>
<span data-ttu-id="b8a0c-108">Azure Vpnsite nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b8a0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8a0c-109">EXAMPLES</span></span>

### <span data-ttu-id="b8a0c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8a0c-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="b8a0c-111">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'deki 1 VpnSiteLinks 'e sahip bir kaynak grubu, sanal WAN ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="b8a0c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8a0c-112">PARAMETERS</span></span>

### <span data-ttu-id="b8a0c-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="b8a0c-113">-BGPAsn</span></span>
<span data-ttu-id="b8a0c-114">Bu Vpnsite için BGP ASN.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-114">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a0c-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b8a0c-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="b8a0c-116">Bu Vpnsite için BGP eşleme adresi.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-116">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="b8a0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a0c-117">-DefaultProfile</span></span>
<span data-ttu-id="b8a0c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a0c-119">-FQDN</span><span class="sxs-lookup"><span data-stu-id="b8a0c-119">-Fqdn</span></span>
<span data-ttu-id="b8a0c-120">Sonraki atlama FQDN 'Si.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a0c-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="b8a0c-121">-IPAddress</span></span>
<span data-ttu-id="b8a0c-122">Sonraki atlama IP adresi.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a0c-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="b8a0c-123">-LinkProviderName</span></span>
<span data-ttu-id="b8a0c-124">Bağlantı sağlayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-124">Link Provider Name.</span></span>

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

### <span data-ttu-id="b8a0c-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="b8a0c-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="b8a0c-126">Mbps cinsinden bağlantı hızı.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-126">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a0c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8a0c-127">-Name</span></span>
<span data-ttu-id="b8a0c-128">Adlandır</span><span class="sxs-lookup"><span data-stu-id="b8a0c-128">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a0c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a0c-129">CommonParameters</span></span>
<span data-ttu-id="b8a0c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a0c-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a0c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8a0c-132">INPUTS</span></span>

### <span data-ttu-id="b8a0c-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b8a0c-133">None</span></span>

## <span data-ttu-id="b8a0c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8a0c-134">OUTPUTS</span></span>

### <span data-ttu-id="b8a0c-135">Microsoft. Azure. Commands. Network. model. Psvpnsite</span><span class="sxs-lookup"><span data-stu-id="b8a0c-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="b8a0c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8a0c-136">NOTES</span></span>

## <span data-ttu-id="b8a0c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8a0c-137">RELATED LINKS</span></span>

[<span data-ttu-id="b8a0c-138">Yeni-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b8a0c-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)