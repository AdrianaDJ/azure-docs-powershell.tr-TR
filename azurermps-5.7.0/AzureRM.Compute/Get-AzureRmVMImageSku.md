---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764480"
---
# <span data-ttu-id="19623-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="19623-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="19623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19623-102">SYNOPSIS</span></span>
<span data-ttu-id="19623-103">Vmımage STB 'Lerini alır.</span><span class="sxs-lookup"><span data-stu-id="19623-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19623-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19623-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="19623-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19623-105">DESCRIPTION</span></span>
<span data-ttu-id="19623-106">**Get-AzureRmVMImageSku** cmdlet 'ı VMImage STB 'lerini alır.</span><span class="sxs-lookup"><span data-stu-id="19623-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="19623-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19623-107">EXAMPLES</span></span>

### <span data-ttu-id="19623-108">Örnek 1: Vmımage STB 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="19623-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="19623-109">Bu komut belirtilen yayımcının STB 'Larını alır ve sunar.</span><span class="sxs-lookup"><span data-stu-id="19623-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="19623-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19623-110">PARAMETERS</span></span>

### <span data-ttu-id="19623-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="19623-111">-Location</span></span>
<span data-ttu-id="19623-112">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="19623-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="19623-113">-Teklif</span><span class="sxs-lookup"><span data-stu-id="19623-113">-Offer</span></span>
<span data-ttu-id="19623-114">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19623-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="19623-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="19623-115">-PublisherName</span></span>
<span data-ttu-id="19623-116">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19623-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="19623-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19623-117">CommonParameters</span></span>
<span data-ttu-id="19623-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19623-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19623-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19623-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19623-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19623-120">INPUTS</span></span>

### <span data-ttu-id="19623-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="19623-121">None</span></span>
<span data-ttu-id="19623-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="19623-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19623-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19623-123">OUTPUTS</span></span>

## <span data-ttu-id="19623-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19623-124">NOTES</span></span>

## <span data-ttu-id="19623-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19623-125">RELATED LINKS</span></span>

[<span data-ttu-id="19623-126">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="19623-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="19623-127">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="19623-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="19623-128">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="19623-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="19623-129">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="19623-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


