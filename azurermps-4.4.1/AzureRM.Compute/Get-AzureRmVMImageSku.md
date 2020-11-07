---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765197"
---
# <span data-ttu-id="faf8a-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="faf8a-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="faf8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf8a-102">SYNOPSIS</span></span>
<span data-ttu-id="faf8a-103">Vmımage STB 'Lerini alır.</span><span class="sxs-lookup"><span data-stu-id="faf8a-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faf8a-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="faf8a-105">DESCRIPTION</span></span>
<span data-ttu-id="faf8a-106">**Get-AzureRmVMImageSku** cmdlet 'ı VMImage STB 'lerini alır.</span><span class="sxs-lookup"><span data-stu-id="faf8a-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="faf8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faf8a-107">EXAMPLES</span></span>

### <span data-ttu-id="faf8a-108">Örnek 1: Vmımage STB 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="faf8a-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="faf8a-109">Bu komut belirtilen yayımcının STB 'Larını alır ve sunar.</span><span class="sxs-lookup"><span data-stu-id="faf8a-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="faf8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faf8a-110">PARAMETERS</span></span>

### <span data-ttu-id="faf8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf8a-111">-DefaultProfile</span></span>
<span data-ttu-id="faf8a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="faf8a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf8a-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="faf8a-113">-Location</span></span>
<span data-ttu-id="faf8a-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf8a-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="faf8a-115">-Teklif</span><span class="sxs-lookup"><span data-stu-id="faf8a-115">-Offer</span></span>
<span data-ttu-id="faf8a-116">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf8a-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="faf8a-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="faf8a-117">-PublisherName</span></span>
<span data-ttu-id="faf8a-118">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf8a-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="faf8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf8a-119">CommonParameters</span></span>
<span data-ttu-id="faf8a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faf8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf8a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf8a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf8a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faf8a-122">INPUTS</span></span>

## <span data-ttu-id="faf8a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faf8a-123">OUTPUTS</span></span>

## <span data-ttu-id="faf8a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faf8a-124">NOTES</span></span>

## <span data-ttu-id="faf8a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faf8a-125">RELATED LINKS</span></span>

[<span data-ttu-id="faf8a-126">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="faf8a-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="faf8a-127">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="faf8a-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="faf8a-128">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="faf8a-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="faf8a-129">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="faf8a-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


