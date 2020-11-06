---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571786"
---
# <span data-ttu-id="cca9f-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cca9f-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="cca9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca9f-102">SYNOPSIS</span></span>
<span data-ttu-id="cca9f-103">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="cca9f-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="cca9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cca9f-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="cca9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cca9f-105">DESCRIPTION</span></span>
<span data-ttu-id="cca9f-106">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="cca9f-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="cca9f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cca9f-107">EXAMPLES</span></span>

### <span data-ttu-id="cca9f-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cca9f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="cca9f-109">Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir</span><span class="sxs-lookup"><span data-stu-id="cca9f-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="cca9f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cca9f-110">PARAMETERS</span></span>

### <span data-ttu-id="cca9f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="cca9f-111">-Name</span></span>
<span data-ttu-id="cca9f-112">Doğrulanacak kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cca9f-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="cca9f-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cca9f-113">-ResourceType</span></span>
<span data-ttu-id="cca9f-114">Doğrulanacak kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="cca9f-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="cca9f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca9f-115">CommonParameters</span></span>
<span data-ttu-id="cca9f-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cca9f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca9f-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca9f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca9f-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cca9f-118">INPUTS</span></span>

## <span data-ttu-id="cca9f-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cca9f-119">OUTPUTS</span></span>

### <span data-ttu-id="cca9f-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Checknamekullanılabilirliği Bilityresponse</span><span class="sxs-lookup"><span data-stu-id="cca9f-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="cca9f-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cca9f-121">NOTES</span></span>

## <span data-ttu-id="cca9f-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cca9f-122">RELATED LINKS</span></span>

