---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098360"
---
# <span data-ttu-id="4c88f-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4c88f-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="4c88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c88f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c88f-103">Vmımage STB 'Lerini alır.</span><span class="sxs-lookup"><span data-stu-id="4c88f-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="4c88f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c88f-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c88f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c88f-105">DESCRIPTION</span></span>
<span data-ttu-id="4c88f-106">**Get-AzVMImageSku** cmdlet 'ı VMImage STB 'lerini alır.</span><span class="sxs-lookup"><span data-stu-id="4c88f-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="4c88f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c88f-107">EXAMPLES</span></span>

### <span data-ttu-id="4c88f-108">Örnek 1: Vmımage STB 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="4c88f-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="4c88f-109">Bu komut belirtilen yayımcının STB 'Larını alır ve sunar.</span><span class="sxs-lookup"><span data-stu-id="4c88f-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="4c88f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c88f-110">PARAMETERS</span></span>

### <span data-ttu-id="4c88f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c88f-111">-DefaultProfile</span></span>
<span data-ttu-id="4c88f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c88f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c88f-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="4c88f-113">-Location</span></span>
<span data-ttu-id="4c88f-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c88f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4c88f-115">-Teklif</span><span class="sxs-lookup"><span data-stu-id="4c88f-115">-Offer</span></span>
<span data-ttu-id="4c88f-116">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c88f-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="4c88f-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4c88f-117">-PublisherName</span></span>
<span data-ttu-id="4c88f-118">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c88f-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="4c88f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c88f-119">CommonParameters</span></span>
<span data-ttu-id="4c88f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c88f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c88f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c88f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c88f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c88f-122">INPUTS</span></span>

### <span data-ttu-id="4c88f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4c88f-123">System.String</span></span>

## <span data-ttu-id="4c88f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c88f-124">OUTPUTS</span></span>

### <span data-ttu-id="4c88f-125">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımaku</span><span class="sxs-lookup"><span data-stu-id="4c88f-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="4c88f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c88f-126">NOTES</span></span>

## <span data-ttu-id="4c88f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c88f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c88f-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4c88f-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="4c88f-129">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="4c88f-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="4c88f-130">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4c88f-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="4c88f-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4c88f-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

