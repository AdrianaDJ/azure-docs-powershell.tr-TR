---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266578"
---
# <span data-ttu-id="cb9ca-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cb9ca-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cb9ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ca-103">Azure 'dan Azure ExpressRoute çapraz bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="cb9ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb9ca-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9ca-106">**Get-AzExpressRouteCrossConnection** cmdlet 'i aboneliğinizden bir ExpressRoute çapraz bağlantı nesnesi almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="cb9ca-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cb9ca-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cb9ca-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb9ca-108">EXAMPLES</span></span>

### <span data-ttu-id="cb9ca-109">Örnek 1: ExpressRoute çapraz bağlantısını alma</span><span class="sxs-lookup"><span data-stu-id="cb9ca-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="cb9ca-110">Örnek 2: filtre kullanarak ExpressRoute çapraz bağlantılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="cb9ca-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="cb9ca-111">Bu cmdlet, "test" ile başlayan tüm ExpressRoute çapraz bağlantılarını listeler</span><span class="sxs-lookup"><span data-stu-id="cb9ca-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="cb9ca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb9ca-112">PARAMETERS</span></span>

### <span data-ttu-id="cb9ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9ca-113">-DefaultProfile</span></span>
<span data-ttu-id="cb9ca-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9ca-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb9ca-115">-Name</span></span>
<span data-ttu-id="cb9ca-116">ExpressRoute çapraz bağlantı adı.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="cb9ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb9ca-118">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="cb9ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ca-119">CommonParameters</span></span>
<span data-ttu-id="cb9ca-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ca-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ca-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb9ca-122">INPUTS</span></span>

### <span data-ttu-id="cb9ca-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cb9ca-123">None</span></span>
<span data-ttu-id="cb9ca-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cb9ca-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb9ca-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb9ca-125">OUTPUTS</span></span>

### <span data-ttu-id="cb9ca-126">Microsoft. Azure. Commands. Network. model. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cb9ca-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cb9ca-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb9ca-127">NOTES</span></span>

## <span data-ttu-id="cb9ca-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb9ca-128">RELATED LINKS</span></span>

[<span data-ttu-id="cb9ca-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cb9ca-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)