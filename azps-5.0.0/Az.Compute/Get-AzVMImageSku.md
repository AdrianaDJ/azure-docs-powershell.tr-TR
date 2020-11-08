---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276252"
---
# <span data-ttu-id="01619-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="01619-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="01619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01619-102">SYNOPSIS</span></span>
<span data-ttu-id="01619-103">Vmımage STB 'Lerini alır.</span><span class="sxs-lookup"><span data-stu-id="01619-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="01619-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01619-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01619-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01619-105">DESCRIPTION</span></span>
<span data-ttu-id="01619-106">**Get-AzVMImageSku** cmdlet 'ı VMImage STB 'lerini alır.</span><span class="sxs-lookup"><span data-stu-id="01619-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="01619-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01619-107">EXAMPLES</span></span>

### <span data-ttu-id="01619-108">Örnek 1: Vmımage STB 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="01619-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="01619-109">Bu komut belirtilen yayımcının STB 'Larını alır ve sunar.</span><span class="sxs-lookup"><span data-stu-id="01619-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="01619-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01619-110">PARAMETERS</span></span>

### <span data-ttu-id="01619-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01619-111">-DefaultProfile</span></span>
<span data-ttu-id="01619-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01619-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01619-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="01619-113">-Location</span></span>
<span data-ttu-id="01619-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01619-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="01619-115">-Teklif</span><span class="sxs-lookup"><span data-stu-id="01619-115">-Offer</span></span>
<span data-ttu-id="01619-116">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="01619-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="01619-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="01619-117">-PublisherName</span></span>
<span data-ttu-id="01619-118">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01619-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="01619-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01619-119">CommonParameters</span></span>
<span data-ttu-id="01619-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01619-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01619-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="01619-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01619-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01619-122">INPUTS</span></span>

### <span data-ttu-id="01619-123">System. String</span><span class="sxs-lookup"><span data-stu-id="01619-123">System.String</span></span>

## <span data-ttu-id="01619-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01619-124">OUTPUTS</span></span>

### <span data-ttu-id="01619-125">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımaku</span><span class="sxs-lookup"><span data-stu-id="01619-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="01619-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01619-126">NOTES</span></span>

## <span data-ttu-id="01619-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01619-127">RELATED LINKS</span></span>

[<span data-ttu-id="01619-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="01619-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="01619-129">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="01619-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="01619-130">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="01619-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="01619-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="01619-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


