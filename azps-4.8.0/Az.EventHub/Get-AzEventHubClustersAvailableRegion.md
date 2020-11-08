---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274534"
---
# <span data-ttu-id="8c545-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="8c545-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="8c545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c545-102">SYNOPSIS</span></span>
<span data-ttu-id="8c545-103">Tek bir Eventhub kümesinin ayrıntılarını veya verilen kaynak grubundaki kümelerin listesini alır</span><span class="sxs-lookup"><span data-stu-id="8c545-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="8c545-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c545-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c545-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c545-105">DESCRIPTION</span></span>
<span data-ttu-id="8c545-106">Adanmış olarak atanmış olan bölgelerin Get-AzEventHubClustersAvailableRegion cmdlet listesi.</span><span class="sxs-lookup"><span data-stu-id="8c545-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="8c545-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c545-107">EXAMPLES</span></span>

### <span data-ttu-id="8c545-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8c545-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="8c545-109">Bölge listesi</span><span class="sxs-lookup"><span data-stu-id="8c545-109">List of regions is returned where</span></span>

## <span data-ttu-id="8c545-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c545-110">PARAMETERS</span></span>

### <span data-ttu-id="8c545-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c545-111">-DefaultProfile</span></span>
<span data-ttu-id="8c545-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c545-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c545-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c545-113">CommonParameters</span></span>
<span data-ttu-id="8c545-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c545-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c545-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c545-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c545-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c545-116">INPUTS</span></span>

### <span data-ttu-id="8c545-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8c545-117">None</span></span>

## <span data-ttu-id="8c545-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c545-118">OUTPUTS</span></span>

### <span data-ttu-id="8c545-119">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. model. 1.5.0.0; Thubsavailablecluster, Microsoft. Azure. PowerShell. cmdlet. EventHub, Version =, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8c545-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8c545-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c545-120">NOTES</span></span>

## <span data-ttu-id="8c545-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c545-121">RELATED LINKS</span></span>
