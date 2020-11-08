---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098361"
---
# <span data-ttu-id="609c6-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="609c6-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="609c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609c6-102">SYNOPSIS</span></span>
<span data-ttu-id="609c6-103">VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="609c6-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="609c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="609c6-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="609c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="609c6-105">DESCRIPTION</span></span>
<span data-ttu-id="609c6-106">**Get-AzVMImagePublisher** cmdlet 'ı VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="609c6-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="609c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="609c6-107">EXAMPLES</span></span>

### <span data-ttu-id="609c6-108">Örnek 1: bölge için Vmımage yayımcıları alma</span><span class="sxs-lookup"><span data-stu-id="609c6-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="609c6-109">Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="609c6-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="609c6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="609c6-110">PARAMETERS</span></span>

### <span data-ttu-id="609c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609c6-111">-DefaultProfile</span></span>
<span data-ttu-id="609c6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="609c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="609c6-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="609c6-113">-Location</span></span>
<span data-ttu-id="609c6-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="609c6-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="609c6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609c6-115">CommonParameters</span></span>
<span data-ttu-id="609c6-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="609c6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609c6-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="609c6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609c6-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="609c6-118">INPUTS</span></span>

### <span data-ttu-id="609c6-119">System. String</span><span class="sxs-lookup"><span data-stu-id="609c6-119">System.String</span></span>

## <span data-ttu-id="609c6-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="609c6-120">OUTPUTS</span></span>

### <span data-ttu-id="609c6-121">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagepublisher</span><span class="sxs-lookup"><span data-stu-id="609c6-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="609c6-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="609c6-122">NOTES</span></span>

## <span data-ttu-id="609c6-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="609c6-123">RELATED LINKS</span></span>

[<span data-ttu-id="609c6-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="609c6-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="609c6-125">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="609c6-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="609c6-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="609c6-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="609c6-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="609c6-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

