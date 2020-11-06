---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586989"
---
# <span data-ttu-id="b954f-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b954f-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="b954f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b954f-102">SYNOPSIS</span></span>
<span data-ttu-id="b954f-103">Vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b954f-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b954f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b954f-104">SYNTAX</span></span>

### <span data-ttu-id="b954f-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="b954f-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b954f-106">Getvmımagedetail</span><span class="sxs-lookup"><span data-stu-id="b954f-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b954f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b954f-107">DESCRIPTION</span></span>
<span data-ttu-id="b954f-108">**Get-Azurermvmımage** cmdlet 'ı bir vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b954f-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b954f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b954f-109">EXAMPLES</span></span>

### <span data-ttu-id="b954f-110">Örnek 1: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="b954f-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="b954f-111">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b954f-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="b954f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b954f-112">PARAMETERS</span></span>

### <span data-ttu-id="b954f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b954f-113">-DefaultProfile</span></span>
<span data-ttu-id="b954f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b954f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b954f-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="b954f-115">-FilterExpression</span></span>
<span data-ttu-id="b954f-116">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b954f-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="b954f-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="b954f-117">-Location</span></span>
<span data-ttu-id="b954f-118">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b954f-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="b954f-119">-Teklif</span><span class="sxs-lookup"><span data-stu-id="b954f-119">-Offer</span></span>
<span data-ttu-id="b954f-120">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b954f-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="b954f-121">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b954f-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="b954f-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b954f-122">-PublisherName</span></span>
<span data-ttu-id="b954f-123">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b954f-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="b954f-124">Resim yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b954f-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b954f-125">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="b954f-125">-Skus</span></span>
<span data-ttu-id="b954f-126">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="b954f-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="b954f-127">SKU edinmek için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b954f-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="b954f-128">-Version</span><span class="sxs-lookup"><span data-stu-id="b954f-128">-Version</span></span>
<span data-ttu-id="b954f-129">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b954f-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="b954f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b954f-130">CommonParameters</span></span>
<span data-ttu-id="b954f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b954f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b954f-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b954f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b954f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b954f-133">INPUTS</span></span>

## <span data-ttu-id="b954f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b954f-134">OUTPUTS</span></span>

## <span data-ttu-id="b954f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b954f-135">NOTES</span></span>

## <span data-ttu-id="b954f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b954f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b954f-137">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="b954f-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="b954f-138">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="b954f-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="b954f-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b954f-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="b954f-140">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="b954f-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


