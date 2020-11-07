---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762158"
---
# <span data-ttu-id="c32e7-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="c32e7-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="c32e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c32e7-103">Sanal makinedeki Market planı bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c32e7-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c32e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c32e7-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c32e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c32e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c32e7-106">**Set-AzureRmVMPlan** cmdlet 'i, sanal makine Için Azure Market planı bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c32e7-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="c32e7-107">Bir Pazaryeri yansımasını komut satırı aracılığıyla dağıtabilmek için, programlı erişimin etkinleştirilmiş olması veya sanal makinenin Azure portalı kullanılarak dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c32e7-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="c32e7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c32e7-108">EXAMPLES</span></span>

## <span data-ttu-id="c32e7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c32e7-109">PARAMETERS</span></span>

### <span data-ttu-id="c32e7-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="c32e7-110">-Name</span></span>
<span data-ttu-id="c32e7-111">Marketten resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32e7-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="c32e7-112">Bu, Get-AzureRmVMImageSku cmdlet tarafından döndürülen değerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c32e7-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="c32e7-113">Görüntü bilgilerini bulma hakkında daha fazla bilgi için, Microsoft Azure belgelerinde [PowerShell Ile Azure sanal makine görüntülerini ve Azure CLI 'Yi seçin](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) .</span><span class="sxs-lookup"><span data-stu-id="c32e7-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32e7-114">-Ürün</span><span class="sxs-lookup"><span data-stu-id="c32e7-114">-Product</span></span>
<span data-ttu-id="c32e7-115">Marketten resmin çarpımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32e7-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="c32e7-116">Bu, **ImageReference** öğesinin **teklif** değeriyle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c32e7-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32e7-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="c32e7-117">-PromotionCode</span></span>
<span data-ttu-id="c32e7-118">Promosyon kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32e7-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32e7-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c32e7-119">-Publisher</span></span>
<span data-ttu-id="c32e7-120">Resmin yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32e7-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="c32e7-121">Bu bilgileri Get-AzureRmVMImagePublisher cmdlet 'i kullanarak bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c32e7-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32e7-122">-VM</span><span class="sxs-lookup"><span data-stu-id="c32e7-122">-VM</span></span>
<span data-ttu-id="c32e7-123">Market planı ayarlanacak sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32e7-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="c32e7-124">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c32e7-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="c32e7-125">Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c32e7-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c32e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32e7-126">CommonParameters</span></span>
<span data-ttu-id="c32e7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c32e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32e7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c32e7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32e7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c32e7-129">INPUTS</span></span>

### <span data-ttu-id="c32e7-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c32e7-130">None</span></span>
<span data-ttu-id="c32e7-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c32e7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c32e7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c32e7-132">OUTPUTS</span></span>

## <span data-ttu-id="c32e7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c32e7-133">NOTES</span></span>

## <span data-ttu-id="c32e7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c32e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="c32e7-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c32e7-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c32e7-136">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="c32e7-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c32e7-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c32e7-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c32e7-138">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c32e7-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
