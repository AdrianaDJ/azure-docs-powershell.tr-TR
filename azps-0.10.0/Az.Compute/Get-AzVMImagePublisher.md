---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: dcb5913176af352c39867f7029523765aca0d781
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937014"
---
# <span data-ttu-id="4b39e-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4b39e-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="4b39e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b39e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b39e-103">VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b39e-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="4b39e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b39e-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b39e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b39e-105">DESCRIPTION</span></span>
<span data-ttu-id="4b39e-106">**Get-AzVMImagePublisher** cmdlet 'ı VMImage yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b39e-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="4b39e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b39e-107">EXAMPLES</span></span>

### <span data-ttu-id="4b39e-108">Örnek 1: bölge için Vmımage yayımcıları alma</span><span class="sxs-lookup"><span data-stu-id="4b39e-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="4b39e-109">Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b39e-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="4b39e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b39e-110">PARAMETERS</span></span>

### <span data-ttu-id="4b39e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b39e-111">-DefaultProfile</span></span>
<span data-ttu-id="4b39e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b39e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b39e-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b39e-113">-Location</span></span>
<span data-ttu-id="4b39e-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b39e-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4b39e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b39e-115">CommonParameters</span></span>
<span data-ttu-id="4b39e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b39e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b39e-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b39e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b39e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b39e-118">INPUTS</span></span>

### <span data-ttu-id="4b39e-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4b39e-119">None</span></span>
<span data-ttu-id="4b39e-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4b39e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b39e-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b39e-121">OUTPUTS</span></span>

### <span data-ttu-id="4b39e-122">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4b39e-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="4b39e-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b39e-123">NOTES</span></span>

## <span data-ttu-id="4b39e-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b39e-124">RELATED LINKS</span></span>

[<span data-ttu-id="4b39e-125">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4b39e-125">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="4b39e-126">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="4b39e-126">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="4b39e-127">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4b39e-127">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="4b39e-128">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4b39e-128">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


