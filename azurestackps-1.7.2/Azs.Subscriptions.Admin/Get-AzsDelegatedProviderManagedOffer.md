---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57e195f1d42b4d1df26344133c10d7c0d40e1f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751303"
---
# <span data-ttu-id="a1e8b-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="a1e8b-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="a1e8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e8b-103">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="a1e8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1e8b-104">SYNTAX</span></span>

### <span data-ttu-id="a1e8b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1e8b-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1e8b-106">Al</span><span class="sxs-lookup"><span data-stu-id="a1e8b-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="a1e8b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a1e8b-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a1e8b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1e8b-108">DESCRIPTION</span></span>
<span data-ttu-id="a1e8b-109">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="a1e8b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1e8b-110">EXAMPLES</span></span>

### <span data-ttu-id="a1e8b-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a1e8b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a1e8b-112">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="a1e8b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1e8b-113">PARAMETERS</span></span>

### <span data-ttu-id="a1e8b-114">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="a1e8b-114">-DelegatedProviderId</span></span>
<span data-ttu-id="a1e8b-115">Temsilci kimliği.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="a1e8b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1e8b-116">-Name</span></span>
<span data-ttu-id="a1e8b-117">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-117">Name of an offer.</span></span>

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

### <span data-ttu-id="a1e8b-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a1e8b-118">-ResourceId</span></span>
<span data-ttu-id="a1e8b-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-119">The resource id.</span></span>

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

### <span data-ttu-id="a1e8b-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="a1e8b-120">-Skip</span></span>
<span data-ttu-id="a1e8b-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a1e8b-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="a1e8b-122">-Top</span></span>
<span data-ttu-id="a1e8b-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a1e8b-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a1e8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e8b-125">CommonParameters</span></span>
<span data-ttu-id="a1e8b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e8b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e8b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e8b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1e8b-128">INPUTS</span></span>

## <span data-ttu-id="a1e8b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1e8b-129">OUTPUTS</span></span>

### <span data-ttu-id="a1e8b-130">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Delegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="a1e8b-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="a1e8b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1e8b-131">NOTES</span></span>

## <span data-ttu-id="a1e8b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1e8b-132">RELATED LINKS</span></span>

