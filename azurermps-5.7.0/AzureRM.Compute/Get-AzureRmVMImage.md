---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587623"
---
# <span data-ttu-id="389b4-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="389b4-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="389b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="389b4-102">SYNOPSIS</span></span>
<span data-ttu-id="389b4-103">Vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="389b4-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="389b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="389b4-104">SYNTAX</span></span>

### <span data-ttu-id="389b4-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="389b4-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="389b4-106">Getvmımagedetail</span><span class="sxs-lookup"><span data-stu-id="389b4-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="389b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="389b4-107">DESCRIPTION</span></span>
<span data-ttu-id="389b4-108">**Get-Azurermvmımage** cmdlet 'ı bir vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="389b4-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="389b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="389b4-109">EXAMPLES</span></span>

### <span data-ttu-id="389b4-110">Örnek 1: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="389b4-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="389b4-111">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="389b4-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="389b4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="389b4-112">PARAMETERS</span></span>

### <span data-ttu-id="389b4-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="389b4-113">-FilterExpression</span></span>
<span data-ttu-id="389b4-114">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="389b4-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389b4-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="389b4-115">-Location</span></span>
<span data-ttu-id="389b4-116">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="389b4-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389b4-117">-Teklif</span><span class="sxs-lookup"><span data-stu-id="389b4-117">-Offer</span></span>
<span data-ttu-id="389b4-118">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="389b4-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="389b4-119">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="389b4-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389b4-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="389b4-120">-PublisherName</span></span>
<span data-ttu-id="389b4-121">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="389b4-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="389b4-122">Resim yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="389b4-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389b4-123">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="389b4-123">-Skus</span></span>
<span data-ttu-id="389b4-124">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="389b4-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="389b4-125">SKU edinmek için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="389b4-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389b4-126">-Version</span><span class="sxs-lookup"><span data-stu-id="389b4-126">-Version</span></span>
<span data-ttu-id="389b4-127">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="389b4-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389b4-128">CommonParameters</span></span>
<span data-ttu-id="389b4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="389b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389b4-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="389b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389b4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="389b4-131">INPUTS</span></span>

### <span data-ttu-id="389b4-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="389b4-132">None</span></span>
<span data-ttu-id="389b4-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="389b4-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="389b4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="389b4-134">OUTPUTS</span></span>

## <span data-ttu-id="389b4-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="389b4-135">NOTES</span></span>

## <span data-ttu-id="389b4-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="389b4-136">RELATED LINKS</span></span>

[<span data-ttu-id="389b4-137">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="389b4-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="389b4-138">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="389b4-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="389b4-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="389b4-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="389b4-140">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="389b4-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


