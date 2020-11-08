---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106412"
---
# <span data-ttu-id="b6cc7-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="b6cc7-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="b6cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cc7-103">Sanal ağ geçidi için IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="b6cc7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6cc7-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6cc7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="b6cc7-106">**Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet 'i sanal ağ geçidi için IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="b6cc7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6cc7-107">EXAMPLES</span></span>

## <span data-ttu-id="b6cc7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6cc7-108">PARAMETERS</span></span>

### <span data-ttu-id="b6cc7-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="b6cc7-109">-ConnectedEntityId</span></span>
<span data-ttu-id="b6cc7-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="b6cc7-111">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="b6cc7-111">-EncryptionType</span></span>
<span data-ttu-id="b6cc7-112">Sanal ağ geçidi için şifreleme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="b6cc7-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b6cc7-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6cc7-114">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="b6cc7-114">NoEncryption</span></span>
- <span data-ttu-id="b6cc7-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="b6cc7-115">RequireEncryption</span></span>

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

### <span data-ttu-id="b6cc7-116">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="b6cc7-116">-GatewayId</span></span>
<span data-ttu-id="b6cc7-117">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="b6cc7-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="b6cc7-118">-PfsGroup</span></span>
<span data-ttu-id="b6cc7-119">Kusursuz iletme gizliliği (PFS) grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="b6cc7-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b6cc7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6cc7-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="b6cc7-121">PFS1</span></span>
- <span data-ttu-id="b6cc7-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6cc7-122">None</span></span>

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

### <span data-ttu-id="b6cc7-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6cc7-123">-Profile</span></span>
<span data-ttu-id="b6cc7-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b6cc7-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6cc7-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="b6cc7-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="b6cc7-127">Güvenlik ilişkisinin (SA) boyutunu kilobayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="b6cc7-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="b6cc7-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="b6cc7-129">Güvenlik ilişkisinin süresini saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="b6cc7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cc7-130">CommonParameters</span></span>
<span data-ttu-id="b6cc7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6cc7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cc7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cc7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cc7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6cc7-133">INPUTS</span></span>

## <span data-ttu-id="b6cc7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6cc7-134">OUTPUTS</span></span>

## <span data-ttu-id="b6cc7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6cc7-135">NOTES</span></span>

## <span data-ttu-id="b6cc7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6cc7-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6cc7-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="b6cc7-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


