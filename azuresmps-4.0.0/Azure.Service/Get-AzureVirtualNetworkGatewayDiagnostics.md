---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106520"
---
# <span data-ttu-id="305ff-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="305ff-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="305ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305ff-102">SYNOPSIS</span></span>
<span data-ttu-id="305ff-103">Azure sanal ağ geçidi Tanılamaların sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="305ff-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="305ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="305ff-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="305ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="305ff-105">DESCRIPTION</span></span>
<span data-ttu-id="305ff-106">**Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet 'i Azure sanal ağ geçidi Tanılamaların sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="305ff-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="305ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="305ff-107">EXAMPLES</span></span>

## <span data-ttu-id="305ff-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="305ff-108">PARAMETERS</span></span>

### <span data-ttu-id="305ff-109">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="305ff-109">-GatewayId</span></span>
<span data-ttu-id="305ff-110">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="305ff-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="305ff-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="305ff-111">-Profile</span></span>
<span data-ttu-id="305ff-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="305ff-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="305ff-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="305ff-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="305ff-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305ff-114">CommonParameters</span></span>
<span data-ttu-id="305ff-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="305ff-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305ff-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305ff-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305ff-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="305ff-117">INPUTS</span></span>

## <span data-ttu-id="305ff-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="305ff-118">OUTPUTS</span></span>

## <span data-ttu-id="305ff-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="305ff-119">NOTES</span></span>

## <span data-ttu-id="305ff-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="305ff-120">RELATED LINKS</span></span>

[<span data-ttu-id="305ff-121">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="305ff-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="305ff-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="305ff-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


