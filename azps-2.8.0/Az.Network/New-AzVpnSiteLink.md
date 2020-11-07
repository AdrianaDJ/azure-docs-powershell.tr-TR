---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918147"
---
# <span data-ttu-id="b7ed3-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b7ed3-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="b7ed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ed3-103">Azure Vpnsite nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b7ed3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7ed3-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7ed3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ed3-106">Azure Vpnsite nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b7ed3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7ed3-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ed3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7ed3-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="b7ed3-109">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'deki 1 VpnSiteLinks 'e sahip bir kaynak grubu, sanal WAN ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="b7ed3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7ed3-110">PARAMETERS</span></span>

### <span data-ttu-id="b7ed3-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="b7ed3-111">-BGPAsn</span></span>
<span data-ttu-id="b7ed3-112">Bu Vpnsite için BGP ASN.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="b7ed3-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b7ed3-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="b7ed3-114">Bu Vpnsite için BGP eşleme adresi.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="b7ed3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ed3-115">-DefaultProfile</span></span>
<span data-ttu-id="b7ed3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ed3-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="b7ed3-117">-IPAddress</span></span>
<span data-ttu-id="b7ed3-118">Sonraki atlama IP adresi.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="b7ed3-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="b7ed3-119">-LinkProviderName</span></span>
<span data-ttu-id="b7ed3-120">Bağlantı sağlayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="b7ed3-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="b7ed3-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="b7ed3-122">Mbps cinsinden bağlantı hızı.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="b7ed3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7ed3-123">-Name</span></span>
<span data-ttu-id="b7ed3-124">Adlandır</span><span class="sxs-lookup"><span data-stu-id="b7ed3-124">Name</span></span>

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

### <span data-ttu-id="b7ed3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ed3-125">CommonParameters</span></span>
<span data-ttu-id="b7ed3-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ed3-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7ed3-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ed3-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7ed3-128">INPUTS</span></span>

### <span data-ttu-id="b7ed3-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7ed3-129">None</span></span>

## <span data-ttu-id="b7ed3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7ed3-130">OUTPUTS</span></span>

### <span data-ttu-id="b7ed3-131">Microsoft. Azure. Commands. Network. model. Psvpnsite</span><span class="sxs-lookup"><span data-stu-id="b7ed3-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="b7ed3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7ed3-132">NOTES</span></span>

## <span data-ttu-id="b7ed3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7ed3-133">RELATED LINKS</span></span>

[<span data-ttu-id="b7ed3-134">Yeni-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b7ed3-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)