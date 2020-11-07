---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940273"
---
# <span data-ttu-id="b89d5-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="b89d5-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="b89d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b89d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b89d5-103">Azure Marketi 'nden indirilen ürünlerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b89d5-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="b89d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b89d5-104">SYNTAX</span></span>

### <span data-ttu-id="b89d5-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b89d5-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b89d5-106">Al</span><span class="sxs-lookup"><span data-stu-id="b89d5-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="b89d5-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b89d5-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b89d5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b89d5-108">DESCRIPTION</span></span>
<span data-ttu-id="b89d5-109">Azure Marketi 'nden indirilen ürünlerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b89d5-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="b89d5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b89d5-110">EXAMPLES</span></span>

### <span data-ttu-id="b89d5-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b89d5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b89d5-112">Indirilen Azure Bridge ürünleri listesini alma</span><span class="sxs-lookup"><span data-stu-id="b89d5-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="b89d5-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b89d5-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="b89d5-114">Bir Azure Köprüsü edinin adıyla Indirildi</span><span class="sxs-lookup"><span data-stu-id="b89d5-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="b89d5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b89d5-115">PARAMETERS</span></span>

### <span data-ttu-id="b89d5-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="b89d5-116">-ActivationName</span></span>
<span data-ttu-id="b89d5-117">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="b89d5-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b89d5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b89d5-118">-Name</span></span>
<span data-ttu-id="b89d5-119">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="b89d5-119">Name of the product.</span></span>

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

### <span data-ttu-id="b89d5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89d5-120">-ResourceGroupName</span></span>
<span data-ttu-id="b89d5-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b89d5-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b89d5-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b89d5-122">-ResourceId</span></span>
<span data-ttu-id="b89d5-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b89d5-123">The resource id.</span></span>

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

### <span data-ttu-id="b89d5-124">-Atla</span><span class="sxs-lookup"><span data-stu-id="b89d5-124">-Skip</span></span>
<span data-ttu-id="b89d5-125">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="b89d5-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b89d5-126">-Üst</span><span class="sxs-lookup"><span data-stu-id="b89d5-126">-Top</span></span>
<span data-ttu-id="b89d5-127">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="b89d5-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b89d5-128">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b89d5-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b89d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89d5-129">CommonParameters</span></span>
<span data-ttu-id="b89d5-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b89d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89d5-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89d5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89d5-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b89d5-132">INPUTS</span></span>

## <span data-ttu-id="b89d5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b89d5-133">OUTPUTS</span></span>

### <span data-ttu-id="b89d5-134">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="b89d5-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="b89d5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b89d5-135">NOTES</span></span>

## <span data-ttu-id="b89d5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b89d5-136">RELATED LINKS</span></span>

