---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594306"
---
# <span data-ttu-id="2fa7f-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2fa7f-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="2fa7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa7f-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa7f-103">VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2fa7f-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fa7f-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fa7f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fa7f-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa7f-106">**Get-Azurermvmımagepublisher** cmdlet 'ı VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2fa7f-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="2fa7f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fa7f-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa7f-108">Örnek 1: bölge için Vmımage yayımcıları alma</span><span class="sxs-lookup"><span data-stu-id="2fa7f-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="2fa7f-109">Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2fa7f-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="2fa7f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fa7f-110">PARAMETERS</span></span>

### <span data-ttu-id="2fa7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa7f-111">-DefaultProfile</span></span>
<span data-ttu-id="2fa7f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fa7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa7f-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="2fa7f-113">-Location</span></span>
<span data-ttu-id="2fa7f-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa7f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="2fa7f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa7f-115">CommonParameters</span></span>
<span data-ttu-id="2fa7f-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fa7f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa7f-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa7f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa7f-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fa7f-118">INPUTS</span></span>

## <span data-ttu-id="2fa7f-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fa7f-119">OUTPUTS</span></span>

## <span data-ttu-id="2fa7f-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fa7f-120">NOTES</span></span>

## <span data-ttu-id="2fa7f-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fa7f-121">RELATED LINKS</span></span>

[<span data-ttu-id="2fa7f-122">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="2fa7f-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="2fa7f-123">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="2fa7f-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="2fa7f-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2fa7f-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="2fa7f-125">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="2fa7f-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


