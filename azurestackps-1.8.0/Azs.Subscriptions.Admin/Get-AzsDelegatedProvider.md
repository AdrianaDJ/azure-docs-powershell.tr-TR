---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934789"
---
# <span data-ttu-id="b87ce-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="b87ce-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="b87ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b87ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b87ce-103">Temsilci sağlayıcıların listesini alın.</span><span class="sxs-lookup"><span data-stu-id="b87ce-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="b87ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b87ce-104">SYNTAX</span></span>

### <span data-ttu-id="b87ce-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b87ce-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="b87ce-106">Al</span><span class="sxs-lookup"><span data-stu-id="b87ce-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="b87ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b87ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b87ce-108">Temsilci sağlayıcıların listesini alın.</span><span class="sxs-lookup"><span data-stu-id="b87ce-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="b87ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b87ce-109">EXAMPLES</span></span>

### <span data-ttu-id="b87ce-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b87ce-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="b87ce-111">Temsilci sağlayıcıların bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="b87ce-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="b87ce-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b87ce-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="b87ce-113">Belirli bir temsilci sağlayıcı edinin.</span><span class="sxs-lookup"><span data-stu-id="b87ce-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="b87ce-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b87ce-114">PARAMETERS</span></span>

### <span data-ttu-id="b87ce-115">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="b87ce-115">-DelegatedProviderId</span></span>
<span data-ttu-id="b87ce-116">{{Fill Delegateıd açıklama}}</span><span class="sxs-lookup"><span data-stu-id="b87ce-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87ce-117">CommonParameters</span></span>
<span data-ttu-id="b87ce-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b87ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87ce-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b87ce-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87ce-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b87ce-120">INPUTS</span></span>

## <span data-ttu-id="b87ce-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b87ce-121">OUTPUTS</span></span>

### <span data-ttu-id="b87ce-122">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="b87ce-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="b87ce-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b87ce-123">NOTES</span></span>

## <span data-ttu-id="b87ce-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b87ce-124">RELATED LINKS</span></span>

