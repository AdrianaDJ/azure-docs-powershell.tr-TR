---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939803"
---
# <span data-ttu-id="fd30b-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fd30b-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="fd30b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd30b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd30b-103">VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fd30b-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd30b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd30b-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd30b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd30b-105">DESCRIPTION</span></span>
<span data-ttu-id="fd30b-106">**Get-Azurermvmımagepublisher** cmdlet 'ı VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fd30b-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="fd30b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd30b-107">EXAMPLES</span></span>

### <span data-ttu-id="fd30b-108">Örnek 1: bölge için Vmımage yayımcıları alma</span><span class="sxs-lookup"><span data-stu-id="fd30b-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="fd30b-109">Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fd30b-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="fd30b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd30b-110">PARAMETERS</span></span>

### <span data-ttu-id="fd30b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd30b-111">-DefaultProfile</span></span>
<span data-ttu-id="fd30b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd30b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd30b-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="fd30b-113">-Location</span></span>
<span data-ttu-id="fd30b-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd30b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="fd30b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd30b-115">CommonParameters</span></span>
<span data-ttu-id="fd30b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd30b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd30b-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd30b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd30b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd30b-118">INPUTS</span></span>

### <span data-ttu-id="fd30b-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fd30b-119">None</span></span>
<span data-ttu-id="fd30b-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fd30b-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd30b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd30b-121">OUTPUTS</span></span>

### <span data-ttu-id="fd30b-122">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagepublisher</span><span class="sxs-lookup"><span data-stu-id="fd30b-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="fd30b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd30b-123">NOTES</span></span>

## <span data-ttu-id="fd30b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd30b-124">RELATED LINKS</span></span>

[<span data-ttu-id="fd30b-125">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="fd30b-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fd30b-126">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="fd30b-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fd30b-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fd30b-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fd30b-128">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="fd30b-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


