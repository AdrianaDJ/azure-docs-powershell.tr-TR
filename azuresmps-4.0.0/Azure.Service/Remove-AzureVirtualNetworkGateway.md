---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F2CADC2-1053-404F-96DA-D992AA39D0FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d410a521d1fd4032b647650b12cfc764aa52e0ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105486"
---
# <span data-ttu-id="a6c91-101">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6c91-101">Remove-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="a6c91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c91-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c91-103">Sanal ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6c91-103">Removes a virtual network gateway.</span></span>

## <span data-ttu-id="a6c91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6c91-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6c91-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6c91-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c91-106">**Remove-AzureVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6c91-106">The **Remove-AzureVirtualNetworkGateway** cmdlet removes a virtual network gateway.</span></span>

## <span data-ttu-id="a6c91-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6c91-107">EXAMPLES</span></span>

## <span data-ttu-id="a6c91-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6c91-108">PARAMETERS</span></span>

### <span data-ttu-id="a6c91-109">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="a6c91-109">-GatewayId</span></span>
<span data-ttu-id="a6c91-110">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6c91-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="a6c91-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="a6c91-111">-Profile</span></span>
<span data-ttu-id="a6c91-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6c91-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a6c91-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a6c91-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6c91-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c91-114">CommonParameters</span></span>
<span data-ttu-id="a6c91-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6c91-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c91-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c91-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c91-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6c91-117">INPUTS</span></span>

## <span data-ttu-id="a6c91-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6c91-118">OUTPUTS</span></span>

## <span data-ttu-id="a6c91-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6c91-119">NOTES</span></span>

## <span data-ttu-id="a6c91-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6c91-120">RELATED LINKS</span></span>

[<span data-ttu-id="a6c91-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6c91-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a6c91-122">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6c91-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a6c91-123">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6c91-123">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


