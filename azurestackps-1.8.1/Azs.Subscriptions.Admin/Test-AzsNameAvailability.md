---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935138"
---
# <span data-ttu-id="3f183-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3f183-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="3f183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f183-102">SYNOPSIS</span></span>
<span data-ttu-id="3f183-103">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="3f183-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="3f183-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f183-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="3f183-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f183-105">DESCRIPTION</span></span>
<span data-ttu-id="3f183-106">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="3f183-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="3f183-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f183-107">EXAMPLES</span></span>

### <span data-ttu-id="3f183-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f183-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="3f183-109">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="3f183-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="3f183-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f183-110">PARAMETERS</span></span>

### <span data-ttu-id="3f183-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f183-111">-Name</span></span>
<span data-ttu-id="3f183-112">Doğrulanacak kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3f183-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="3f183-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3f183-113">-ResourceType</span></span>
<span data-ttu-id="3f183-114">Doğrulanacak kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="3f183-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="3f183-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f183-115">CommonParameters</span></span>
<span data-ttu-id="3f183-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f183-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f183-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f183-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f183-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f183-118">INPUTS</span></span>

## <span data-ttu-id="3f183-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f183-119">OUTPUTS</span></span>

### <span data-ttu-id="3f183-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Checknamekullanılabilirliği Bilityresponse</span><span class="sxs-lookup"><span data-stu-id="3f183-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="3f183-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f183-121">NOTES</span></span>

## <span data-ttu-id="3f183-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f183-122">RELATED LINKS</span></span>

