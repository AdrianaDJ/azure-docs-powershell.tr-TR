---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940265"
---
# <span data-ttu-id="2868c-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="2868c-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="2868c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2868c-102">SYNOPSIS</span></span>
<span data-ttu-id="2868c-103">Azure Marketi 'nden indirilen bir ürünü silme.</span><span class="sxs-lookup"><span data-stu-id="2868c-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="2868c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2868c-104">SYNTAX</span></span>

### <span data-ttu-id="2868c-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2868c-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2868c-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2868c-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2868c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2868c-107">DESCRIPTION</span></span>
<span data-ttu-id="2868c-108">Azure Marketi 'nden indirilen bir ürünü silme.</span><span class="sxs-lookup"><span data-stu-id="2868c-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="2868c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2868c-109">EXAMPLES</span></span>

### <span data-ttu-id="2868c-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="2868c-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="2868c-111">Azure Marketi 'nden indirilen bir ürünü silme</span><span class="sxs-lookup"><span data-stu-id="2868c-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="2868c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2868c-112">PARAMETERS</span></span>

### <span data-ttu-id="2868c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2868c-113">-Name</span></span>
<span data-ttu-id="2868c-114">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="2868c-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="2868c-115">-ActivationName</span></span>
<span data-ttu-id="2868c-116">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="2868c-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2868c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2868c-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2868c-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2868c-119">-Force</span></span>
<span data-ttu-id="2868c-120">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="2868c-120">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2868c-121">-ResourceId</span></span>
<span data-ttu-id="2868c-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2868c-122">The resource id.</span></span>

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

### <span data-ttu-id="2868c-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="2868c-123">-AsJob</span></span>
<span data-ttu-id="2868c-124">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="2868c-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2868c-125">-WhatIf</span></span>
<span data-ttu-id="2868c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2868c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2868c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2868c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="2868c-128">-Confirm</span></span>
<span data-ttu-id="2868c-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2868c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2868c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2868c-130">CommonParameters</span></span>
<span data-ttu-id="2868c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2868c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2868c-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2868c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2868c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2868c-133">INPUTS</span></span>

## <span data-ttu-id="2868c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2868c-134">OUTPUTS</span></span>

### <span data-ttu-id="2868c-135">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="2868c-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="2868c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2868c-136">NOTES</span></span>

## <span data-ttu-id="2868c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2868c-137">RELATED LINKS</span></span>