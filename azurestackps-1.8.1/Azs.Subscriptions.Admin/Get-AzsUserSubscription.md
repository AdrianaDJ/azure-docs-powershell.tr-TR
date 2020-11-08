---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934921"
---
# <span data-ttu-id="78982-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="78982-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="78982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78982-102">SYNOPSIS</span></span>
<span data-ttu-id="78982-103">Kullanıcı abonelikleri listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="78982-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="78982-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78982-104">SYNTAX</span></span>

### <span data-ttu-id="78982-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78982-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="78982-106">Al</span><span class="sxs-lookup"><span data-stu-id="78982-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="78982-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="78982-107">DESCRIPTION</span></span>
<span data-ttu-id="78982-108">Kullanıcı abonelikleri listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="78982-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="78982-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78982-109">EXAMPLES</span></span>

### <span data-ttu-id="78982-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="78982-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="78982-111">Kullanıcı abonelikleri listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="78982-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="78982-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78982-112">PARAMETERS</span></span>

### <span data-ttu-id="78982-113">-Filtre</span><span class="sxs-lookup"><span data-stu-id="78982-113">-Filter</span></span>
<span data-ttu-id="78982-114">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="78982-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="78982-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="78982-115">-SubscriptionId</span></span>
<span data-ttu-id="78982-116">Abonelik kimliği parametresi.</span><span class="sxs-lookup"><span data-stu-id="78982-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="78982-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78982-117">CommonParameters</span></span>
<span data-ttu-id="78982-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78982-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78982-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78982-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78982-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78982-120">INPUTS</span></span>

## <span data-ttu-id="78982-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78982-121">OUTPUTS</span></span>

### <span data-ttu-id="78982-122">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="78982-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="78982-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78982-123">NOTES</span></span>

## <span data-ttu-id="78982-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78982-124">RELATED LINKS</span></span>
