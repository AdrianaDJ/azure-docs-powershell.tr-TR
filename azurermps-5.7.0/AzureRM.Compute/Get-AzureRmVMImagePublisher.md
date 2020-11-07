---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764479"
---
# <span data-ttu-id="07174-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="07174-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="07174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07174-102">SYNOPSIS</span></span>
<span data-ttu-id="07174-103">VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="07174-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07174-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07174-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="07174-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07174-105">DESCRIPTION</span></span>
<span data-ttu-id="07174-106">**Get-Azurermvmımagepublisher** cmdlet 'ı VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="07174-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="07174-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07174-107">EXAMPLES</span></span>

### <span data-ttu-id="07174-108">Örnek 1: bölge için Vmımage yayımcıları alma</span><span class="sxs-lookup"><span data-stu-id="07174-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="07174-109">Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="07174-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="07174-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07174-110">PARAMETERS</span></span>

### <span data-ttu-id="07174-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="07174-111">-Location</span></span>
<span data-ttu-id="07174-112">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07174-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="07174-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07174-113">CommonParameters</span></span>
<span data-ttu-id="07174-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07174-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07174-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07174-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07174-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07174-116">INPUTS</span></span>

### <span data-ttu-id="07174-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07174-117">None</span></span>
<span data-ttu-id="07174-118">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="07174-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07174-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07174-119">OUTPUTS</span></span>

## <span data-ttu-id="07174-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07174-120">NOTES</span></span>

## <span data-ttu-id="07174-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07174-121">RELATED LINKS</span></span>

[<span data-ttu-id="07174-122">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="07174-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="07174-123">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="07174-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="07174-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="07174-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="07174-125">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="07174-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


