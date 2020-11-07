---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934566"
---
# <span data-ttu-id="73f88-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="73f88-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="73f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73f88-102">SYNOPSIS</span></span>
<span data-ttu-id="73f88-103">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="73f88-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="73f88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73f88-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="73f88-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73f88-105">DESCRIPTION</span></span>
<span data-ttu-id="73f88-106">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="73f88-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="73f88-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73f88-107">EXAMPLES</span></span>

### <span data-ttu-id="73f88-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="73f88-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="73f88-109">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="73f88-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="73f88-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73f88-110">PARAMETERS</span></span>

### <span data-ttu-id="73f88-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="73f88-111">-Name</span></span>
<span data-ttu-id="73f88-112">Doğrulanacak kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="73f88-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="73f88-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="73f88-113">-ResourceType</span></span>
<span data-ttu-id="73f88-114">Doğrulanacak kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="73f88-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="73f88-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f88-115">CommonParameters</span></span>
<span data-ttu-id="73f88-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73f88-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f88-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f88-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f88-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73f88-118">INPUTS</span></span>

## <span data-ttu-id="73f88-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73f88-119">OUTPUTS</span></span>

### <span data-ttu-id="73f88-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Checknamekullanılabilirliği Bilityresponse</span><span class="sxs-lookup"><span data-stu-id="73f88-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="73f88-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73f88-121">NOTES</span></span>

## <span data-ttu-id="73f88-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73f88-122">RELATED LINKS</span></span>

