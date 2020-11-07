---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940269"
---
# <span data-ttu-id="f6efc-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="f6efc-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="f6efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6efc-102">SYNOPSIS</span></span>
<span data-ttu-id="f6efc-103">Azure Marketi 'nden indirilen bir ürünü silme.</span><span class="sxs-lookup"><span data-stu-id="f6efc-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="f6efc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6efc-104">SYNTAX</span></span>

### <span data-ttu-id="f6efc-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6efc-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6efc-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f6efc-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6efc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6efc-107">DESCRIPTION</span></span>
<span data-ttu-id="f6efc-108">Azure Marketi 'nden indirilen bir ürünü silme.</span><span class="sxs-lookup"><span data-stu-id="f6efc-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="f6efc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6efc-109">EXAMPLES</span></span>

### <span data-ttu-id="f6efc-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f6efc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="f6efc-111">Azure Marketi 'nden indirilen bir ürünü silme</span><span class="sxs-lookup"><span data-stu-id="f6efc-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="f6efc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6efc-112">PARAMETERS</span></span>

### <span data-ttu-id="f6efc-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="f6efc-113">-ActivationName</span></span>
<span data-ttu-id="f6efc-114">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="f6efc-114">Name of the activation.</span></span>

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

### <span data-ttu-id="f6efc-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f6efc-115">-AsJob</span></span>
<span data-ttu-id="f6efc-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="f6efc-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f6efc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f6efc-117">-Force</span></span>
<span data-ttu-id="f6efc-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="f6efc-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f6efc-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6efc-119">-Name</span></span>
<span data-ttu-id="f6efc-120">Ürünün adı.</span><span class="sxs-lookup"><span data-stu-id="f6efc-120">Name of the product.</span></span>

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

### <span data-ttu-id="f6efc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6efc-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6efc-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f6efc-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f6efc-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f6efc-123">-ResourceId</span></span>
<span data-ttu-id="f6efc-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f6efc-124">The resource id.</span></span>

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

### <span data-ttu-id="f6efc-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6efc-125">-Confirm</span></span>
<span data-ttu-id="f6efc-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6efc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6efc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6efc-127">-WhatIf</span></span>
<span data-ttu-id="f6efc-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6efc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6efc-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6efc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6efc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6efc-130">CommonParameters</span></span>
<span data-ttu-id="f6efc-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6efc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6efc-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6efc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6efc-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6efc-133">INPUTS</span></span>

## <span data-ttu-id="f6efc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6efc-134">OUTPUTS</span></span>

### <span data-ttu-id="f6efc-135">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="f6efc-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="f6efc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6efc-136">NOTES</span></span>

## <span data-ttu-id="f6efc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6efc-137">RELATED LINKS</span></span>

