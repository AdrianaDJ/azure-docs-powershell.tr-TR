---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934943"
---
# <span data-ttu-id="1135a-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="1135a-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="1135a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1135a-102">SYNOPSIS</span></span>
<span data-ttu-id="1135a-103">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="1135a-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1135a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1135a-104">SYNTAX</span></span>

### <span data-ttu-id="1135a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1135a-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1135a-106">Al</span><span class="sxs-lookup"><span data-stu-id="1135a-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="1135a-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1135a-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1135a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1135a-108">DESCRIPTION</span></span>
<span data-ttu-id="1135a-109">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="1135a-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1135a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1135a-110">EXAMPLES</span></span>

### <span data-ttu-id="1135a-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1135a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="1135a-112">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="1135a-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1135a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1135a-113">PARAMETERS</span></span>

### <span data-ttu-id="1135a-114">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="1135a-114">-DelegatedProviderId</span></span>
<span data-ttu-id="1135a-115">Temsilci kimliği.</span><span class="sxs-lookup"><span data-stu-id="1135a-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="1135a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1135a-116">-Name</span></span>
<span data-ttu-id="1135a-117">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="1135a-117">Name of an offer.</span></span>

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

### <span data-ttu-id="1135a-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1135a-118">-ResourceId</span></span>
<span data-ttu-id="1135a-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1135a-119">The resource id.</span></span>

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

### <span data-ttu-id="1135a-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="1135a-120">-Skip</span></span>
<span data-ttu-id="1135a-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="1135a-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1135a-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="1135a-122">-Top</span></span>
<span data-ttu-id="1135a-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="1135a-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1135a-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1135a-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1135a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1135a-125">CommonParameters</span></span>
<span data-ttu-id="1135a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1135a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1135a-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1135a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1135a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1135a-128">INPUTS</span></span>

## <span data-ttu-id="1135a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1135a-129">OUTPUTS</span></span>

### <span data-ttu-id="1135a-130">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Delegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="1135a-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="1135a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1135a-131">NOTES</span></span>

## <span data-ttu-id="1135a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1135a-132">RELATED LINKS</span></span>

