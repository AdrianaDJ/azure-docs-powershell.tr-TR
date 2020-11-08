---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105437"
---
# <span data-ttu-id="d5c23-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d5c23-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="d5c23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c23-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c23-103">Azure sanal ağ geçidi için anahtarı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d5c23-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="d5c23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5c23-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5c23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5c23-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c23-106">**Set-AzureVirtualNetworkGatewayKey** cmdlet 'ı bir Azure sanal ağ geçidi için anahtarı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d5c23-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="d5c23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5c23-107">EXAMPLES</span></span>

## <span data-ttu-id="d5c23-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5c23-108">PARAMETERS</span></span>

### <span data-ttu-id="d5c23-109">-Connectedentityıd</span><span class="sxs-lookup"><span data-stu-id="d5c23-109">-ConnectedEntityId</span></span>
<span data-ttu-id="d5c23-110">Bağlı bir varlığın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5c23-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="d5c23-111">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="d5c23-111">-GatewayId</span></span>
<span data-ttu-id="d5c23-112">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5c23-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d5c23-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5c23-113">-Profile</span></span>
<span data-ttu-id="d5c23-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5c23-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d5c23-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d5c23-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5c23-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d5c23-116">-SharedKey</span></span>
<span data-ttu-id="d5c23-117">Paylaşılan bir anahtar belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5c23-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="d5c23-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c23-118">CommonParameters</span></span>
<span data-ttu-id="d5c23-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5c23-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c23-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c23-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c23-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5c23-121">INPUTS</span></span>

## <span data-ttu-id="d5c23-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5c23-122">OUTPUTS</span></span>

## <span data-ttu-id="d5c23-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5c23-123">NOTES</span></span>

## <span data-ttu-id="d5c23-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5c23-124">RELATED LINKS</span></span>

[<span data-ttu-id="d5c23-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d5c23-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="d5c23-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d5c23-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


