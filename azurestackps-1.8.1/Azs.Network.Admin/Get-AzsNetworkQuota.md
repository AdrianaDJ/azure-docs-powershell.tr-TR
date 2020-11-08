---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935087"
---
# <span data-ttu-id="f44ae-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="f44ae-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="f44ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f44ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f44ae-103">Tüm kotaları listeler.</span><span class="sxs-lookup"><span data-stu-id="f44ae-103">List all quotas.</span></span>

## <span data-ttu-id="f44ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f44ae-104">SYNTAX</span></span>

### <span data-ttu-id="f44ae-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f44ae-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="f44ae-106">Al</span><span class="sxs-lookup"><span data-stu-id="f44ae-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="f44ae-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f44ae-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f44ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f44ae-108">DESCRIPTION</span></span>
<span data-ttu-id="f44ae-109">Tüm kotaları listeler.</span><span class="sxs-lookup"><span data-stu-id="f44ae-109">List all quotas.</span></span>
<span data-ttu-id="f44ae-110">Adı veya filtreyi geçirerek listeyi sınırlayın.</span><span class="sxs-lookup"><span data-stu-id="f44ae-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="f44ae-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f44ae-111">EXAMPLES</span></span>

### <span data-ttu-id="f44ae-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="f44ae-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="f44ae-113">Tüm ağ kotalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f44ae-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="f44ae-114">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="f44ae-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="f44ae-115">Belirtilen ağ kotasını alır.</span><span class="sxs-lookup"><span data-stu-id="f44ae-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="f44ae-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f44ae-116">PARAMETERS</span></span>

### <span data-ttu-id="f44ae-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f44ae-117">-Name</span></span>
<span data-ttu-id="f44ae-118">Ağ kotası kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f44ae-118">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f44ae-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="f44ae-119">-Location</span></span>
<span data-ttu-id="f44ae-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f44ae-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f44ae-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f44ae-121">-ResourceId</span></span>
<span data-ttu-id="f44ae-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f44ae-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44ae-123">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f44ae-123">-Filter</span></span>
<span data-ttu-id="f44ae-124">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="f44ae-124">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f44ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44ae-125">CommonParameters</span></span>
<span data-ttu-id="f44ae-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f44ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44ae-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44ae-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44ae-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f44ae-128">INPUTS</span></span>

## <span data-ttu-id="f44ae-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f44ae-129">OUTPUTS</span></span>

### <span data-ttu-id="f44ae-130">Microsoft. AzureStack. Management. Network. admin. modeller. Quota</span><span class="sxs-lookup"><span data-stu-id="f44ae-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="f44ae-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f44ae-131">NOTES</span></span>

## <span data-ttu-id="f44ae-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f44ae-132">RELATED LINKS</span></span>