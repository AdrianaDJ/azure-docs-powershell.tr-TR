---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107090"
---
# <span data-ttu-id="cff17-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="cff17-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="cff17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff17-102">SYNOPSIS</span></span>
<span data-ttu-id="cff17-103">Temsilci sağlayıcıların listesini alın.</span><span class="sxs-lookup"><span data-stu-id="cff17-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="cff17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cff17-104">SYNTAX</span></span>

### <span data-ttu-id="cff17-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cff17-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="cff17-106">Al</span><span class="sxs-lookup"><span data-stu-id="cff17-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="cff17-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cff17-107">DESCRIPTION</span></span>
<span data-ttu-id="cff17-108">Temsilci sağlayıcıların listesini alın.</span><span class="sxs-lookup"><span data-stu-id="cff17-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="cff17-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cff17-109">EXAMPLES</span></span>

### <span data-ttu-id="cff17-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cff17-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="cff17-111">Temsilci sağlayıcıların bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="cff17-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="cff17-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cff17-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="cff17-113">Belirli bir temsilci sağlayıcı edinin.</span><span class="sxs-lookup"><span data-stu-id="cff17-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="cff17-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cff17-114">PARAMETERS</span></span>

### <span data-ttu-id="cff17-115">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="cff17-115">-DelegatedProviderId</span></span>
<span data-ttu-id="cff17-116">{{Fill Delegateıd açıklama}}</span><span class="sxs-lookup"><span data-stu-id="cff17-116">{{Fill DelegatedProviderId Description}}</span></span>

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

### <span data-ttu-id="cff17-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff17-117">CommonParameters</span></span>
<span data-ttu-id="cff17-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cff17-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff17-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff17-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff17-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cff17-120">INPUTS</span></span>

## <span data-ttu-id="cff17-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cff17-121">OUTPUTS</span></span>

### <span data-ttu-id="cff17-122">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="cff17-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="cff17-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cff17-123">NOTES</span></span>

## <span data-ttu-id="cff17-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cff17-124">RELATED LINKS</span></span>

