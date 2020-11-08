---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106185"
---
# <span data-ttu-id="10a9d-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10a9d-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="10a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="10a9d-103">Azure sanal ağ geçidi ağ bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10a9d-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="10a9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10a9d-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10a9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="10a9d-106">**New-AzureVirtualNetworkGatewayConnection** cmdlet 'ı bir Azure sanal ağ geçidi ağ bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10a9d-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="10a9d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10a9d-107">EXAMPLES</span></span>

## <span data-ttu-id="10a9d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10a9d-108">PARAMETERS</span></span>

### <span data-ttu-id="10a9d-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="10a9d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="10a9d-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="10a9d-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="10a9d-111">-EnableBgp</span></span>
<span data-ttu-id="10a9d-112">Sınır Ağ Geçidi Protokolü 'Nü (BGP) verir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="10a9d-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="10a9d-113">-GatewayConnectionName</span></span>
<span data-ttu-id="10a9d-114">Ağ Geçidi bağlantısı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="10a9d-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="10a9d-115">-GatewayConnectionType</span></span>
<span data-ttu-id="10a9d-116">Ağ Geçidi bağlantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a9d-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="10a9d-117">-Profile</span></span>
<span data-ttu-id="10a9d-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="10a9d-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="10a9d-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10a9d-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="10a9d-120">-RoutingWeight</span></span>
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

### <span data-ttu-id="10a9d-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="10a9d-121">-SharedKey</span></span>
<span data-ttu-id="10a9d-122">Paylaşılan bir anahtar belirtir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="10a9d-123">-Virtualnetworkgatewayıd</span><span class="sxs-lookup"><span data-stu-id="10a9d-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="10a9d-124">Sanal ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="10a9d-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="10a9d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a9d-125">CommonParameters</span></span>
<span data-ttu-id="10a9d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10a9d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a9d-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a9d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a9d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10a9d-128">INPUTS</span></span>

## <span data-ttu-id="10a9d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10a9d-129">OUTPUTS</span></span>

## <span data-ttu-id="10a9d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10a9d-130">NOTES</span></span>

## <span data-ttu-id="10a9d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10a9d-131">RELATED LINKS</span></span>

[<span data-ttu-id="10a9d-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10a9d-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="10a9d-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10a9d-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="10a9d-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10a9d-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


