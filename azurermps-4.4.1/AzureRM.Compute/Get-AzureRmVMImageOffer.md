---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764573"
---
# <span data-ttu-id="58716-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="58716-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="58716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58716-102">SYNOPSIS</span></span>
<span data-ttu-id="58716-103">Vmımage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="58716-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58716-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58716-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58716-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="58716-105">DESCRIPTION</span></span>
<span data-ttu-id="58716-106">**Get-Azurermvmımageteklifini** , VMImage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="58716-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="58716-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58716-107">EXAMPLES</span></span>

### <span data-ttu-id="58716-108">Örnek 1: Yayımcı için teklif türleri alma</span><span class="sxs-lookup"><span data-stu-id="58716-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="58716-109">Bu komut, Merkezi ABD bölgesindeki Belirtilen yayımcının teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="58716-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="58716-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58716-110">PARAMETERS</span></span>

### <span data-ttu-id="58716-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58716-111">-DefaultProfile</span></span>
<span data-ttu-id="58716-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58716-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58716-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="58716-113">-Location</span></span>
<span data-ttu-id="58716-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="58716-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="58716-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="58716-115">-PublisherName</span></span>
<span data-ttu-id="58716-116">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58716-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="58716-117">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="58716-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="58716-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58716-118">CommonParameters</span></span>
<span data-ttu-id="58716-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58716-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58716-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58716-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58716-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58716-121">INPUTS</span></span>

## <span data-ttu-id="58716-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58716-122">OUTPUTS</span></span>

## <span data-ttu-id="58716-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58716-123">NOTES</span></span>

## <span data-ttu-id="58716-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58716-124">RELATED LINKS</span></span>

[<span data-ttu-id="58716-125">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="58716-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="58716-126">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="58716-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="58716-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="58716-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="58716-128">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="58716-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


