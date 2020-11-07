---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939412"
---
# <span data-ttu-id="6dd74-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6dd74-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="6dd74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd74-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd74-103">Vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="6dd74-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dd74-104">SYNTAX</span></span>

### <span data-ttu-id="6dd74-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="6dd74-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dd74-106">Getvmımagedetail</span><span class="sxs-lookup"><span data-stu-id="6dd74-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dd74-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dd74-107">DESCRIPTION</span></span>
<span data-ttu-id="6dd74-108">**Get-Azurermvmımage** cmdlet 'ı bir vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="6dd74-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="6dd74-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dd74-109">EXAMPLES</span></span>

### <span data-ttu-id="6dd74-110">Örnek 1: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="6dd74-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="6dd74-111">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="6dd74-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="6dd74-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dd74-112">PARAMETERS</span></span>

### <span data-ttu-id="6dd74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd74-113">-DefaultProfile</span></span>
<span data-ttu-id="6dd74-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dd74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dd74-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="6dd74-115">-FilterExpression</span></span>
<span data-ttu-id="6dd74-116">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd74-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="6dd74-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="6dd74-117">-Location</span></span>
<span data-ttu-id="6dd74-118">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd74-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="6dd74-119">-Teklif</span><span class="sxs-lookup"><span data-stu-id="6dd74-119">-Offer</span></span>
<span data-ttu-id="6dd74-120">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd74-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="6dd74-121">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6dd74-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="6dd74-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6dd74-122">-PublisherName</span></span>
<span data-ttu-id="6dd74-123">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd74-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="6dd74-124">Resim yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6dd74-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6dd74-125">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="6dd74-125">-Skus</span></span>
<span data-ttu-id="6dd74-126">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd74-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="6dd74-127">SKU edinmek için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6dd74-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="6dd74-128">-Version</span><span class="sxs-lookup"><span data-stu-id="6dd74-128">-Version</span></span>
<span data-ttu-id="6dd74-129">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd74-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="6dd74-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd74-130">CommonParameters</span></span>
<span data-ttu-id="6dd74-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dd74-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd74-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd74-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd74-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dd74-133">INPUTS</span></span>

### <span data-ttu-id="6dd74-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6dd74-134">None</span></span>
<span data-ttu-id="6dd74-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6dd74-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6dd74-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dd74-136">OUTPUTS</span></span>

### <span data-ttu-id="6dd74-137">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımage</span><span class="sxs-lookup"><span data-stu-id="6dd74-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="6dd74-138">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagedetail</span><span class="sxs-lookup"><span data-stu-id="6dd74-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="6dd74-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dd74-139">NOTES</span></span>

## <span data-ttu-id="6dd74-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dd74-140">RELATED LINKS</span></span>

[<span data-ttu-id="6dd74-141">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="6dd74-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="6dd74-142">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="6dd74-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="6dd74-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6dd74-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="6dd74-144">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="6dd74-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


