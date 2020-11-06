---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594127"
---
# <span data-ttu-id="4f9be-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4f9be-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="4f9be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f9be-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9be-103">Vmımage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4f9be-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f9be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f9be-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="4f9be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f9be-105">DESCRIPTION</span></span>
<span data-ttu-id="4f9be-106">**Get-Azurermvmımageteklifini** , VMImage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4f9be-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="4f9be-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f9be-107">EXAMPLES</span></span>

### <span data-ttu-id="4f9be-108">Örnek 1: Yayımcı için teklif türleri alma</span><span class="sxs-lookup"><span data-stu-id="4f9be-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="4f9be-109">Bu komut, Merkezi ABD bölgesindeki Belirtilen yayımcının teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4f9be-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="4f9be-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f9be-110">PARAMETERS</span></span>

### <span data-ttu-id="4f9be-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="4f9be-111">-Location</span></span>
<span data-ttu-id="4f9be-112">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f9be-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4f9be-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4f9be-113">-PublisherName</span></span>
<span data-ttu-id="4f9be-114">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f9be-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4f9be-115">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f9be-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4f9be-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9be-116">CommonParameters</span></span>
<span data-ttu-id="4f9be-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f9be-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9be-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f9be-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9be-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f9be-119">INPUTS</span></span>

### <span data-ttu-id="4f9be-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f9be-120">None</span></span>
<span data-ttu-id="4f9be-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4f9be-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f9be-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f9be-122">OUTPUTS</span></span>

## <span data-ttu-id="4f9be-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f9be-123">NOTES</span></span>

## <span data-ttu-id="4f9be-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f9be-124">RELATED LINKS</span></span>

[<span data-ttu-id="4f9be-125">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="4f9be-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4f9be-126">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4f9be-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4f9be-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4f9be-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4f9be-128">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="4f9be-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


