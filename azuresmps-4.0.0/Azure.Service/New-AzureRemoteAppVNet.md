---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105994"
---
# <span data-ttu-id="2a815-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="2a815-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="2a815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a815-102">SYNOPSIS</span></span>
<span data-ttu-id="2a815-103">Azure RemoteApp sanal ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a815-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="2a815-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a815-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2a815-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a815-105">DESCRIPTION</span></span>
<span data-ttu-id="2a815-106">**Yeni-AzureRemoteAppVNet** cmdlet 'ı Azure RemoteApp sanal ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a815-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="2a815-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a815-107">EXAMPLES</span></span>

### <span data-ttu-id="2a815-108">Örnek 1: sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a815-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="2a815-109">Bu komut, ContosoVNet adında bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a815-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="2a815-110">İşlemin durumunu belirlemek için, **Get-AzureRemoteAppOperationResult** cmdlet 'ini kullanarak bu cmdlet 'in DÖNDÜRDÜĞÜ izleme kimliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a815-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="2a815-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a815-111">PARAMETERS</span></span>

### <span data-ttu-id="2a815-112">-Dnsserverıpaddress</span><span class="sxs-lookup"><span data-stu-id="2a815-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="2a815-113">DNS sunucularının IPv4 adreslerinin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a815-114">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="2a815-114">-GatewayType</span></span>
<span data-ttu-id="2a815-115">Kullanılacak ağ geçidi yönlendirmesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="2a815-116">Bu parametre için kabul edilebilir değerler: StaticRouting veya Dynamıuting.</span><span class="sxs-lookup"><span data-stu-id="2a815-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a815-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="2a815-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="2a815-118">Yerel ağ adresi alanını sınıfsız etki alanları arası yönlendirme (CıDR) gösteriminde belirten bir dizeler dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="2a815-119">Bu adres alanı *Virtualnetworkaddressspace* parametresinin belirttiği sanal ağ adresi alanıyla çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a815-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a815-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="2a815-120">-Location</span></span>
<span data-ttu-id="2a815-121">Sanal ağın oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a815-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2a815-122">-Profile</span></span>
<span data-ttu-id="2a815-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2a815-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2a815-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2a815-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="2a815-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="2a815-126">CıDR gösteriminde sanal ağ adresi alanını belirten bir dize dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="2a815-127">Bu, özel IP adresi aralığında olmalıdır ve *Localnetworkaddressspace* parametresinin belirttiği yerel ağ adresi alanıyla çakışamaz.</span><span class="sxs-lookup"><span data-stu-id="2a815-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a815-128">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="2a815-128">-VNetName</span></span>
<span data-ttu-id="2a815-129">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="2a815-130">-Vpndeviceıpaddress</span><span class="sxs-lookup"><span data-stu-id="2a815-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="2a815-131">Sanal özel ağ (VPN) aygıtının adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a815-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="2a815-132">Bu, genel kullanıma açık bir adres olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a815-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="2a815-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a815-133">CommonParameters</span></span>
<span data-ttu-id="2a815-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a815-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a815-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a815-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a815-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a815-136">INPUTS</span></span>

## <span data-ttu-id="2a815-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a815-137">OUTPUTS</span></span>

## <span data-ttu-id="2a815-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a815-138">NOTES</span></span>

## <span data-ttu-id="2a815-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a815-139">RELATED LINKS</span></span>

[<span data-ttu-id="2a815-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="2a815-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="2a815-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="2a815-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="2a815-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="2a815-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="2a815-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="2a815-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


