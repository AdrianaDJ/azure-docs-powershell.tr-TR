---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106186"
---
# <span data-ttu-id="a5033-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a5033-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="a5033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5033-102">SYNOPSIS</span></span>
<span data-ttu-id="a5033-103">Azure sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5033-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="a5033-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5033-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a5033-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5033-105">DESCRIPTION</span></span>
<span data-ttu-id="a5033-106">**New-AzureVirtualNetworkGateway** cmdlet 'ı bir Azure sanal ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5033-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="a5033-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5033-107">EXAMPLES</span></span>

## <span data-ttu-id="a5033-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5033-108">PARAMETERS</span></span>

### <span data-ttu-id="a5033-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="a5033-109">-Asn</span></span>
<span data-ttu-id="a5033-110">Otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-110">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a5033-111">-Force</span></span>
<span data-ttu-id="a5033-112">Azure sanal ağ geçidi oluşturmayı onaylama</span><span class="sxs-lookup"><span data-stu-id="a5033-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a5033-113">-GatewayName</span></span>
<span data-ttu-id="a5033-114">Ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-114">Specifies the name of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="a5033-115">-GatewaySKU</span></span>
<span data-ttu-id="a5033-116">Bu cmdlet 'in oluşturduğu sanal ağ geçidinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="a5033-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a5033-117">Valid values are:</span></span>

- <span data-ttu-id="a5033-118">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="a5033-118">Default</span></span>
- <span data-ttu-id="a5033-119">Ardından</span><span class="sxs-lookup"><span data-stu-id="a5033-119">Standard</span></span>
- <span data-ttu-id="a5033-120">Üst performans</span><span class="sxs-lookup"><span data-stu-id="a5033-120">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-121">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="a5033-121">-GatewayType</span></span>
<span data-ttu-id="a5033-122">Ağ Geçidi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-122">Specifies the type of gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="a5033-123">-Location</span></span>
<span data-ttu-id="a5033-124">Konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-124">Specifies the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a5033-125">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="a5033-126">-Profile</span></span>
<span data-ttu-id="a5033-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5033-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a5033-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5033-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="a5033-129">-VnetId</span></span>
<span data-ttu-id="a5033-130">Sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-130">Specifies the ID of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-131">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="a5033-131">-VNetName</span></span>
<span data-ttu-id="a5033-132">Sanal ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5033-132">Specifies a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5033-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5033-133">CommonParameters</span></span>
<span data-ttu-id="a5033-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5033-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5033-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5033-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5033-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5033-136">INPUTS</span></span>

## <span data-ttu-id="a5033-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5033-137">OUTPUTS</span></span>

## <span data-ttu-id="a5033-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5033-138">NOTES</span></span>

## <span data-ttu-id="a5033-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5033-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5033-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a5033-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a5033-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a5033-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a5033-142">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a5033-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
