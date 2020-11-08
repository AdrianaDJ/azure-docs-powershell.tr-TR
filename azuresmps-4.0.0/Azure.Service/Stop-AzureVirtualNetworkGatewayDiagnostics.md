---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105740"
---
# <span data-ttu-id="1e520-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e520-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="1e520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e520-102">SYNOPSIS</span></span>
<span data-ttu-id="1e520-103">Çalışan bir sanal ağ geçidi tanılama oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="1e520-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="1e520-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e520-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e520-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e520-105">DESCRIPTION</span></span>
<span data-ttu-id="1e520-106">**Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet 'i, çalışan bir sanal ağ geçidi tanılama oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="1e520-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="1e520-107">Bu komut tanılama oturumunun sonuçlarını Start-AzureVirtualNetworkGatewayDiagnostics cmdlet 'in belirttiği depolama hesabına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1e520-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="1e520-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e520-108">EXAMPLES</span></span>

## <span data-ttu-id="1e520-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e520-109">PARAMETERS</span></span>

### <span data-ttu-id="1e520-110">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="1e520-110">-GatewayId</span></span>
<span data-ttu-id="1e520-111">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e520-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="1e520-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e520-112">-Profile</span></span>
<span data-ttu-id="1e520-113">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e520-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1e520-114">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1e520-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e520-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e520-115">CommonParameters</span></span>
<span data-ttu-id="1e520-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e520-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e520-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e520-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e520-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e520-118">INPUTS</span></span>

## <span data-ttu-id="1e520-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e520-119">OUTPUTS</span></span>

## <span data-ttu-id="1e520-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e520-120">NOTES</span></span>

## <span data-ttu-id="1e520-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e520-121">RELATED LINKS</span></span>

[<span data-ttu-id="1e520-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e520-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="1e520-123">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e520-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


