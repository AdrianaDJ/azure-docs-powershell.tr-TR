---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098939"
---
# <span data-ttu-id="db94f-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db94f-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="db94f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db94f-102">SYNOPSIS</span></span>
<span data-ttu-id="db94f-103">Azure 'dan Azure ExpressRoute çapraz bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="db94f-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="db94f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db94f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db94f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db94f-105">DESCRIPTION</span></span>
<span data-ttu-id="db94f-106">**Get-AzExpressRouteCrossConnection** cmdlet 'i aboneliğinizden bir ExpressRoute çapraz bağlantı nesnesi almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="db94f-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="db94f-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db94f-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="db94f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db94f-108">EXAMPLES</span></span>

### <span data-ttu-id="db94f-109">Örnek 1: ExpressRoute çapraz bağlantısını alma</span><span class="sxs-lookup"><span data-stu-id="db94f-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="db94f-110">Örnek 2: filtre kullanarak ExpressRoute çapraz bağlantılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="db94f-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="db94f-111">Bu cmdlet, "test" ile başlayan tüm ExpressRoute çapraz bağlantılarını listeler</span><span class="sxs-lookup"><span data-stu-id="db94f-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="db94f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db94f-112">PARAMETERS</span></span>

### <span data-ttu-id="db94f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db94f-113">-DefaultProfile</span></span>
<span data-ttu-id="db94f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db94f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db94f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="db94f-115">-Name</span></span>
<span data-ttu-id="db94f-116">ExpressRoute çapraz bağlantı adı.</span><span class="sxs-lookup"><span data-stu-id="db94f-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="db94f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db94f-117">-ResourceGroupName</span></span>
<span data-ttu-id="db94f-118">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="db94f-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="db94f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db94f-119">CommonParameters</span></span>
<span data-ttu-id="db94f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db94f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db94f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db94f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db94f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db94f-122">INPUTS</span></span>

### <span data-ttu-id="db94f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="db94f-123">None</span></span>
<span data-ttu-id="db94f-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="db94f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db94f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db94f-125">OUTPUTS</span></span>

### <span data-ttu-id="db94f-126">Microsoft. Azure. Commands. Network. model. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db94f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="db94f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db94f-127">NOTES</span></span>

## <span data-ttu-id="db94f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db94f-128">RELATED LINKS</span></span>

[<span data-ttu-id="db94f-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="db94f-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)