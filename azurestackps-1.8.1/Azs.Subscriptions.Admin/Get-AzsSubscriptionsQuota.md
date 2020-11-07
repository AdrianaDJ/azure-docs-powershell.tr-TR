---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934923"
---
# <span data-ttu-id="111a0-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="111a0-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="111a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="111a0-102">SYNOPSIS</span></span>
<span data-ttu-id="111a0-103">Bir konumdaki abonelik kaynağı sağlayıcısı kotaları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="111a0-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="111a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="111a0-104">SYNTAX</span></span>

### <span data-ttu-id="111a0-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="111a0-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="111a0-106">Al</span><span class="sxs-lookup"><span data-stu-id="111a0-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="111a0-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="111a0-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="111a0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="111a0-108">DESCRIPTION</span></span>
<span data-ttu-id="111a0-109">Bir konumdaki kotalar listesini alın.</span><span class="sxs-lookup"><span data-stu-id="111a0-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="111a0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="111a0-110">EXAMPLES</span></span>

### <span data-ttu-id="111a0-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="111a0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="111a0-112">Bir konumdaki abonelik kaynağı sağlayıcısı kotaları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="111a0-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="111a0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="111a0-113">PARAMETERS</span></span>

### <span data-ttu-id="111a0-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="111a0-114">-Location</span></span>
<span data-ttu-id="111a0-115">AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="111a0-115">The AzureStack location.</span></span>

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

### <span data-ttu-id="111a0-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="111a0-116">-Name</span></span>
<span data-ttu-id="111a0-117">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="111a0-117">Name of the quota.</span></span>

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

### <span data-ttu-id="111a0-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="111a0-118">-ResourceId</span></span>
<span data-ttu-id="111a0-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="111a0-119">The resource id.</span></span>

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

### <span data-ttu-id="111a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111a0-120">CommonParameters</span></span>
<span data-ttu-id="111a0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="111a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111a0-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="111a0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111a0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="111a0-123">INPUTS</span></span>

## <span data-ttu-id="111a0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="111a0-124">OUTPUTS</span></span>

### <span data-ttu-id="111a0-125">Microsoft. AzureStack. Management. abonelikler. admin. modeller. kota</span><span class="sxs-lookup"><span data-stu-id="111a0-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="111a0-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="111a0-126">NOTES</span></span>

## <span data-ttu-id="111a0-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="111a0-127">RELATED LINKS</span></span>

