---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932026"
---
# <span data-ttu-id="7972b-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7972b-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7972b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7972b-102">SYNOPSIS</span></span>
<span data-ttu-id="7972b-103">Azure 'dan Azure ExpressRoute çapraz bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="7972b-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="7972b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7972b-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7972b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7972b-105">DESCRIPTION</span></span>
<span data-ttu-id="7972b-106">**Get-AzExpressRouteCrossConnection** cmdlet 'i aboneliğinizden bir ExpressRoute çapraz bağlantı nesnesi almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7972b-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="7972b-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7972b-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7972b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7972b-108">EXAMPLES</span></span>

### <span data-ttu-id="7972b-109">Örnek 1: ExpressRoute çapraz bağlantısını alma</span><span class="sxs-lookup"><span data-stu-id="7972b-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="7972b-110">Örnek 2: filtre kullanarak ExpressRoute çapraz bağlantılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="7972b-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="7972b-111">Bu cmdlet, "test" ile başlayan tüm ExpressRoute çapraz bağlantılarını listeler</span><span class="sxs-lookup"><span data-stu-id="7972b-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="7972b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7972b-112">PARAMETERS</span></span>

### <span data-ttu-id="7972b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7972b-113">-DefaultProfile</span></span>
<span data-ttu-id="7972b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7972b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7972b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7972b-115">-Name</span></span>
<span data-ttu-id="7972b-116">ExpressRoute çapraz bağlantı adı.</span><span class="sxs-lookup"><span data-stu-id="7972b-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="7972b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7972b-117">-ResourceGroupName</span></span>
<span data-ttu-id="7972b-118">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7972b-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="7972b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7972b-119">CommonParameters</span></span>
<span data-ttu-id="7972b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7972b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7972b-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7972b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7972b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7972b-122">INPUTS</span></span>

### <span data-ttu-id="7972b-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7972b-123">None</span></span>
<span data-ttu-id="7972b-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7972b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7972b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7972b-125">OUTPUTS</span></span>

### <span data-ttu-id="7972b-126">Microsoft. Azure. Commands. Network. model. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7972b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7972b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7972b-127">NOTES</span></span>

## <span data-ttu-id="7972b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7972b-128">RELATED LINKS</span></span>

[<span data-ttu-id="7972b-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7972b-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)