---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 5ec6b8c01badec3677e77254128db215c0e41554
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917423"
---
# <span data-ttu-id="faad5-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="faad5-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="faad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faad5-102">SYNOPSIS</span></span>
<span data-ttu-id="faad5-103">Vmımage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="faad5-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="faad5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faad5-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="faad5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="faad5-105">DESCRIPTION</span></span>
<span data-ttu-id="faad5-106">**Get-Azvmimageteklifini** , VMImage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="faad5-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="faad5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faad5-107">EXAMPLES</span></span>

### <span data-ttu-id="faad5-108">Örnek 1: Yayımcı için teklif türleri alma</span><span class="sxs-lookup"><span data-stu-id="faad5-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="faad5-109">Bu komut, Merkezi ABD bölgesindeki Belirtilen yayımcının teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="faad5-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="faad5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faad5-110">PARAMETERS</span></span>

### <span data-ttu-id="faad5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faad5-111">-DefaultProfile</span></span>
<span data-ttu-id="faad5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="faad5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faad5-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="faad5-113">-Location</span></span>
<span data-ttu-id="faad5-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="faad5-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="faad5-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="faad5-115">-PublisherName</span></span>
<span data-ttu-id="faad5-116">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faad5-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="faad5-117">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="faad5-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="faad5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faad5-118">CommonParameters</span></span>
<span data-ttu-id="faad5-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faad5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faad5-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="faad5-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faad5-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faad5-121">INPUTS</span></span>

### <span data-ttu-id="faad5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="faad5-122">System.String</span></span>

## <span data-ttu-id="faad5-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faad5-123">OUTPUTS</span></span>

### <span data-ttu-id="faad5-124">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımageteklifini</span><span class="sxs-lookup"><span data-stu-id="faad5-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="faad5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faad5-125">NOTES</span></span>

## <span data-ttu-id="faad5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faad5-126">RELATED LINKS</span></span>

[<span data-ttu-id="faad5-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="faad5-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="faad5-128">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="faad5-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="faad5-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="faad5-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="faad5-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="faad5-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


