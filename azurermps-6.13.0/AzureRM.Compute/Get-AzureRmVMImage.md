---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 881f4ba2d9750c9edbcb988ce3d438e062934a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590955"
---
# <span data-ttu-id="fc420-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fc420-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="fc420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc420-102">SYNOPSIS</span></span>
<span data-ttu-id="fc420-103">Vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fc420-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc420-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc420-104">SYNTAX</span></span>

### <span data-ttu-id="fc420-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="fc420-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc420-106">Getvmımagedetail</span><span class="sxs-lookup"><span data-stu-id="fc420-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc420-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc420-107">DESCRIPTION</span></span>
<span data-ttu-id="fc420-108">**Get-Azurermvmımage** cmdlet 'ı bir vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fc420-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="fc420-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc420-109">EXAMPLES</span></span>

### <span data-ttu-id="fc420-110">Örnek 1: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="fc420-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"
```

<span data-ttu-id="fc420-111">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fc420-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="fc420-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc420-112">PARAMETERS</span></span>

### <span data-ttu-id="fc420-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc420-113">-DefaultProfile</span></span>
<span data-ttu-id="fc420-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc420-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="fc420-115">-FilterExpression</span></span>
<span data-ttu-id="fc420-116">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc420-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="fc420-117">-Location</span></span>
<span data-ttu-id="fc420-118">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc420-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-119">-Teklif</span><span class="sxs-lookup"><span data-stu-id="fc420-119">-Offer</span></span>
<span data-ttu-id="fc420-120">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc420-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="fc420-121">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc420-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fc420-122">-PublisherName</span></span>
<span data-ttu-id="fc420-123">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc420-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="fc420-124">Resim yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc420-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-125">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="fc420-125">-Skus</span></span>
<span data-ttu-id="fc420-126">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc420-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="fc420-127">SKU edinmek için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc420-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-128">-Version</span><span class="sxs-lookup"><span data-stu-id="fc420-128">-Version</span></span>
<span data-ttu-id="fc420-129">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc420-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc420-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc420-130">CommonParameters</span></span>
<span data-ttu-id="fc420-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc420-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc420-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc420-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc420-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc420-133">INPUTS</span></span>

### <span data-ttu-id="fc420-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fc420-134">System.String</span></span>

## <span data-ttu-id="fc420-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc420-135">OUTPUTS</span></span>

### <span data-ttu-id="fc420-136">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımage</span><span class="sxs-lookup"><span data-stu-id="fc420-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="fc420-137">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagedetail</span><span class="sxs-lookup"><span data-stu-id="fc420-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="fc420-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc420-138">NOTES</span></span>

## <span data-ttu-id="fc420-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc420-139">RELATED LINKS</span></span>

[<span data-ttu-id="fc420-140">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="fc420-140">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fc420-141">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="fc420-141">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fc420-142">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fc420-142">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fc420-143">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="fc420-143">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


