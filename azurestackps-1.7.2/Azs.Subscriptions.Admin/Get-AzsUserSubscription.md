---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934506"
---
# <span data-ttu-id="3419b-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="3419b-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="3419b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3419b-102">SYNOPSIS</span></span>
<span data-ttu-id="3419b-103">Kullanıcı abonelikleri listesini işleç olarak alın.</span><span class="sxs-lookup"><span data-stu-id="3419b-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="3419b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3419b-104">SYNTAX</span></span>

### <span data-ttu-id="3419b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3419b-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="3419b-106">Al</span><span class="sxs-lookup"><span data-stu-id="3419b-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="3419b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3419b-107">DESCRIPTION</span></span>
<span data-ttu-id="3419b-108">Kullanıcı abonelikleri listesini işleç olarak alın.</span><span class="sxs-lookup"><span data-stu-id="3419b-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="3419b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3419b-109">EXAMPLES</span></span>

### <span data-ttu-id="3419b-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3419b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="3419b-111">Kullanıcı abonelikleri listesini işleç olarak alın.</span><span class="sxs-lookup"><span data-stu-id="3419b-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="3419b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3419b-112">PARAMETERS</span></span>

### <span data-ttu-id="3419b-113">-Filtre</span><span class="sxs-lookup"><span data-stu-id="3419b-113">-Filter</span></span>
<span data-ttu-id="3419b-114">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="3419b-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="3419b-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3419b-115">-SubscriptionId</span></span>
<span data-ttu-id="3419b-116">Abonelik kimliği parametresi.</span><span class="sxs-lookup"><span data-stu-id="3419b-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3419b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3419b-117">CommonParameters</span></span>
<span data-ttu-id="3419b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3419b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3419b-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3419b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3419b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3419b-120">INPUTS</span></span>

## <span data-ttu-id="3419b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3419b-121">OUTPUTS</span></span>

### <span data-ttu-id="3419b-122">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="3419b-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="3419b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3419b-123">NOTES</span></span>

## <span data-ttu-id="3419b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3419b-124">RELATED LINKS</span></span>

