---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106909"
---
# <span data-ttu-id="2f47b-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="2f47b-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="2f47b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f47b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f47b-103">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2f47b-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="2f47b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f47b-104">SYNTAX</span></span>

### <span data-ttu-id="2f47b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f47b-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f47b-106">Al</span><span class="sxs-lookup"><span data-stu-id="2f47b-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="2f47b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2f47b-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2f47b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f47b-108">DESCRIPTION</span></span>
<span data-ttu-id="2f47b-109">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2f47b-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="2f47b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f47b-110">EXAMPLES</span></span>

### <span data-ttu-id="2f47b-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f47b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="2f47b-112">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2f47b-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="2f47b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f47b-113">PARAMETERS</span></span>

### <span data-ttu-id="2f47b-114">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="2f47b-114">-DelegatedProviderId</span></span>
<span data-ttu-id="2f47b-115">Temsilci kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f47b-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f47b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f47b-116">-Name</span></span>
<span data-ttu-id="2f47b-117">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="2f47b-117">Name of an offer.</span></span>

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

### <span data-ttu-id="2f47b-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2f47b-118">-ResourceId</span></span>
<span data-ttu-id="2f47b-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f47b-119">The resource id.</span></span>

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

### <span data-ttu-id="2f47b-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="2f47b-120">-Skip</span></span>
<span data-ttu-id="2f47b-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="2f47b-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f47b-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="2f47b-122">-Top</span></span>
<span data-ttu-id="2f47b-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="2f47b-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2f47b-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2f47b-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f47b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f47b-125">CommonParameters</span></span>
<span data-ttu-id="2f47b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f47b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f47b-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f47b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f47b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f47b-128">INPUTS</span></span>

## <span data-ttu-id="2f47b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f47b-129">OUTPUTS</span></span>

### <span data-ttu-id="2f47b-130">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Delegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="2f47b-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="2f47b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f47b-131">NOTES</span></span>

## <span data-ttu-id="2f47b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f47b-132">RELATED LINKS</span></span>

