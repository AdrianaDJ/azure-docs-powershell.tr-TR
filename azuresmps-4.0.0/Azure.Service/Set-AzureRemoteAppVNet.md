---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106052"
---
# <span data-ttu-id="b9139-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b9139-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="b9139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9139-102">SYNOPSIS</span></span>
<span data-ttu-id="b9139-103">Azure RemoteApp sanal ağının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b9139-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="b9139-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9139-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b9139-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9139-105">DESCRIPTION</span></span>
<span data-ttu-id="b9139-106">**Set-AzureRemoteAppVNet** cmdlet 'i, bir Azure RemoteApp sanal ağının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b9139-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="b9139-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9139-107">EXAMPLES</span></span>

### <span data-ttu-id="b9139-108">Örnek 1: sanal ağın özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b9139-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="b9139-109">Bu komut, ContosoVNet adlı sanal ağın özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b9139-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="b9139-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9139-110">PARAMETERS</span></span>

### <span data-ttu-id="b9139-111">-Dnsserverıpaddress</span><span class="sxs-lookup"><span data-stu-id="b9139-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="b9139-112">DNS sunucularının IPv4 adreslerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9139-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9139-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="b9139-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="b9139-114">Yerel ağ adresi alanını sınıflar Inter-Domain yönlendirme (CıDR) gösteriminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9139-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="b9139-115">Bu, sanal ağ adresi alanıyla çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="b9139-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9139-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="b9139-116">-Profile</span></span>
<span data-ttu-id="b9139-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9139-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b9139-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b9139-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9139-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="b9139-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="b9139-120">CıDR gösteriminde sanal ağ adresi alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9139-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="b9139-121">Bu, özel IP adresi aralığında olmalıdır ve yerel ağ adresi alanıyla çakışamaz.</span><span class="sxs-lookup"><span data-stu-id="b9139-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9139-122">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="b9139-122">-VNetName</span></span>
<span data-ttu-id="b9139-123">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9139-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9139-124">-Vpndeviceıpaddress</span><span class="sxs-lookup"><span data-stu-id="b9139-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="b9139-125">Sanal özel ağ (VPN) aygıtının adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9139-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="b9139-126">Bu, genel kullanıma açık bir adres olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b9139-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9139-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9139-127">CommonParameters</span></span>
<span data-ttu-id="b9139-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9139-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9139-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9139-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9139-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9139-130">INPUTS</span></span>

## <span data-ttu-id="b9139-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9139-131">OUTPUTS</span></span>

## <span data-ttu-id="b9139-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9139-132">NOTES</span></span>

## <span data-ttu-id="b9139-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9139-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9139-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b9139-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


