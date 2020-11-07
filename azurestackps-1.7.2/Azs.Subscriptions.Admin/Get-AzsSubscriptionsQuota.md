---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934248"
---
# <span data-ttu-id="011fe-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="011fe-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="011fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="011fe-102">SYNOPSIS</span></span>
<span data-ttu-id="011fe-103">Bir konumdaki abonelik kaynağı sağlayıcısı kotaları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="011fe-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="011fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="011fe-104">SYNTAX</span></span>

### <span data-ttu-id="011fe-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="011fe-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="011fe-106">Al</span><span class="sxs-lookup"><span data-stu-id="011fe-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="011fe-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="011fe-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="011fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="011fe-108">DESCRIPTION</span></span>
<span data-ttu-id="011fe-109">Bir konumdaki kotalar listesini alın.</span><span class="sxs-lookup"><span data-stu-id="011fe-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="011fe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="011fe-110">EXAMPLES</span></span>

### <span data-ttu-id="011fe-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="011fe-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="011fe-112">Bir konumdaki abonelik kaynağı sağlayıcısı kotaları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="011fe-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="011fe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="011fe-113">PARAMETERS</span></span>

### <span data-ttu-id="011fe-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="011fe-114">-Location</span></span>
<span data-ttu-id="011fe-115">AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="011fe-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011fe-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="011fe-116">-Name</span></span>
<span data-ttu-id="011fe-117">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="011fe-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011fe-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="011fe-118">-ResourceId</span></span>
<span data-ttu-id="011fe-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="011fe-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="011fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011fe-120">CommonParameters</span></span>
<span data-ttu-id="011fe-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="011fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011fe-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011fe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011fe-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="011fe-123">INPUTS</span></span>

## <span data-ttu-id="011fe-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="011fe-124">OUTPUTS</span></span>

### <span data-ttu-id="011fe-125">Microsoft. AzureStack. Management. abonelikler. admin. modeller. kota</span><span class="sxs-lookup"><span data-stu-id="011fe-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="011fe-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="011fe-126">NOTES</span></span>

## <span data-ttu-id="011fe-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="011fe-127">RELATED LINKS</span></span>

