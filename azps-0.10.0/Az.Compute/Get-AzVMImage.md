---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937018"
---
# <span data-ttu-id="55888-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="55888-101">Get-AzVMImage</span></span>

## <span data-ttu-id="55888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55888-102">SYNOPSIS</span></span>
<span data-ttu-id="55888-103">Vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="55888-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="55888-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55888-104">SYNTAX</span></span>

### <span data-ttu-id="55888-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="55888-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55888-106">Getvmımagedetail</span><span class="sxs-lookup"><span data-stu-id="55888-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55888-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55888-107">DESCRIPTION</span></span>
<span data-ttu-id="55888-108">**Get-AzVMImage** cmdlet 'ı vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="55888-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="55888-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55888-109">EXAMPLES</span></span>

### <span data-ttu-id="55888-110">Örnek 1: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="55888-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="55888-111">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="55888-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="55888-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55888-112">PARAMETERS</span></span>

### <span data-ttu-id="55888-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55888-113">-DefaultProfile</span></span>
<span data-ttu-id="55888-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55888-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55888-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="55888-115">-FilterExpression</span></span>
<span data-ttu-id="55888-116">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="55888-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="55888-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="55888-117">-Location</span></span>
<span data-ttu-id="55888-118">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55888-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="55888-119">-Teklif</span><span class="sxs-lookup"><span data-stu-id="55888-119">-Offer</span></span>
<span data-ttu-id="55888-120">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55888-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="55888-121">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="55888-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="55888-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="55888-122">-PublisherName</span></span>
<span data-ttu-id="55888-123">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55888-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="55888-124">Resim yayımcısı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="55888-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="55888-125">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="55888-125">-Skus</span></span>
<span data-ttu-id="55888-126">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="55888-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="55888-127">SKU edinmek için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="55888-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="55888-128">-Version</span><span class="sxs-lookup"><span data-stu-id="55888-128">-Version</span></span>
<span data-ttu-id="55888-129">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55888-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="55888-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55888-130">CommonParameters</span></span>
<span data-ttu-id="55888-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55888-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55888-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55888-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55888-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55888-133">INPUTS</span></span>

### <span data-ttu-id="55888-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55888-134">None</span></span>
<span data-ttu-id="55888-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="55888-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55888-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55888-136">OUTPUTS</span></span>

### <span data-ttu-id="55888-137">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımage</span><span class="sxs-lookup"><span data-stu-id="55888-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="55888-138">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagedetail</span><span class="sxs-lookup"><span data-stu-id="55888-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="55888-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55888-139">NOTES</span></span>

## <span data-ttu-id="55888-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55888-140">RELATED LINKS</span></span>

[<span data-ttu-id="55888-141">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="55888-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="55888-142">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="55888-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="55888-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="55888-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="55888-144">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="55888-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


