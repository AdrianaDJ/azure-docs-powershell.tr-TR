---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940257"
---
# <span data-ttu-id="df553-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="df553-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="df553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df553-102">SYNOPSIS</span></span>
<span data-ttu-id="df553-103">Azure Marketi 'nden yüklenebilecek ürünlerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="df553-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="df553-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df553-104">SYNTAX</span></span>

### <span data-ttu-id="df553-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df553-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="df553-106">Al</span><span class="sxs-lookup"><span data-stu-id="df553-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="df553-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="df553-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="df553-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="df553-108">DESCRIPTION</span></span>
<span data-ttu-id="df553-109">Azure Marketi 'nden yüklenebilecek ürünlerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="df553-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="df553-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df553-110">EXAMPLES</span></span>

### <span data-ttu-id="df553-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="df553-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="df553-112">Azure Marketi 'nden yüklenebilecek ürünlerin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="df553-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="df553-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="df553-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="df553-114">Azure Marketi 'nden ada göre yüklenebilecek bir ürün bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="df553-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="df553-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df553-115">PARAMETERS</span></span>

### <span data-ttu-id="df553-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="df553-116">-Name</span></span>
<span data-ttu-id="df553-117">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="df553-117">Name of the product.</span></span>

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

### <span data-ttu-id="df553-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="df553-118">-ActivationName</span></span>
<span data-ttu-id="df553-119">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="df553-119">Name of the activation.</span></span>

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

### <span data-ttu-id="df553-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df553-120">-ResourceGroupName</span></span>
<span data-ttu-id="df553-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="df553-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="df553-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="df553-122">-ResourceId</span></span>
<span data-ttu-id="df553-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="df553-123">The resource id.</span></span>

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

### <span data-ttu-id="df553-124">-Atla</span><span class="sxs-lookup"><span data-stu-id="df553-124">-Skip</span></span>
<span data-ttu-id="df553-125">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="df553-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="df553-126">-Üst</span><span class="sxs-lookup"><span data-stu-id="df553-126">-Top</span></span>
<span data-ttu-id="df553-127">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="df553-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="df553-128">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="df553-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="df553-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df553-129">CommonParameters</span></span>
<span data-ttu-id="df553-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df553-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df553-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df553-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df553-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df553-132">INPUTS</span></span>

## <span data-ttu-id="df553-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df553-133">OUTPUTS</span></span>

### <span data-ttu-id="df553-134">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. ProductResource</span><span class="sxs-lookup"><span data-stu-id="df553-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="df553-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df553-135">NOTES</span></span>

## <span data-ttu-id="df553-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df553-136">RELATED LINKS</span></span>
