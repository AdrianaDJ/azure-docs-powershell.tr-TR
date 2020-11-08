---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106088"
---
# <span data-ttu-id="c770d-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c770d-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="c770d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c770d-102">SYNOPSIS</span></span>
<span data-ttu-id="c770d-103">Sanal ağ geçidi anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c770d-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="c770d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c770d-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c770d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c770d-105">DESCRIPTION</span></span>
<span data-ttu-id="c770d-106">**Reset-AzureVirtualNetworkGatewayKey** cmdlet 'i sanal ağ geçidi anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="c770d-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="c770d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c770d-107">EXAMPLES</span></span>

## <span data-ttu-id="c770d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c770d-108">PARAMETERS</span></span>

### <span data-ttu-id="c770d-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="c770d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c770d-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c770d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="c770d-111">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="c770d-111">-GatewayId</span></span>
<span data-ttu-id="c770d-112">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c770d-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="c770d-113">-keyLength</span><span class="sxs-lookup"><span data-stu-id="c770d-113">-keyLength</span></span>
<span data-ttu-id="c770d-114">Anahtar uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c770d-114">Specifies the key length.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c770d-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="c770d-115">-Profile</span></span>
<span data-ttu-id="c770d-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c770d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c770d-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c770d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c770d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c770d-118">CommonParameters</span></span>
<span data-ttu-id="c770d-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c770d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c770d-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c770d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c770d-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c770d-121">INPUTS</span></span>

## <span data-ttu-id="c770d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c770d-122">OUTPUTS</span></span>

## <span data-ttu-id="c770d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c770d-123">NOTES</span></span>

## <span data-ttu-id="c770d-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c770d-124">RELATED LINKS</span></span>

[<span data-ttu-id="c770d-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c770d-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="c770d-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c770d-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
