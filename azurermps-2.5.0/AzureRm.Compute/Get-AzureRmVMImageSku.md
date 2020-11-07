---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939801"
---
# <span data-ttu-id="f3931-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f3931-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="f3931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3931-102">SYNOPSIS</span></span>
<span data-ttu-id="f3931-103">Vmımage STB 'Lerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3931-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3931-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3931-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3931-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3931-105">DESCRIPTION</span></span>
<span data-ttu-id="f3931-106">**Get-AzureRmVMImageSku** cmdlet 'ı VMImage STB 'lerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3931-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="f3931-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3931-107">EXAMPLES</span></span>

### <span data-ttu-id="f3931-108">Örnek 1: Vmımage STB 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="f3931-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="f3931-109">Bu komut belirtilen yayımcının STB 'Larını alır ve sunar.</span><span class="sxs-lookup"><span data-stu-id="f3931-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="f3931-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3931-110">PARAMETERS</span></span>

### <span data-ttu-id="f3931-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3931-111">-DefaultProfile</span></span>
<span data-ttu-id="f3931-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3931-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3931-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="f3931-113">-Location</span></span>
<span data-ttu-id="f3931-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3931-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f3931-115">-Teklif</span><span class="sxs-lookup"><span data-stu-id="f3931-115">-Offer</span></span>
<span data-ttu-id="f3931-116">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3931-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="f3931-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f3931-117">-PublisherName</span></span>
<span data-ttu-id="f3931-118">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3931-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="f3931-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3931-119">CommonParameters</span></span>
<span data-ttu-id="f3931-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3931-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3931-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3931-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3931-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3931-122">INPUTS</span></span>

### <span data-ttu-id="f3931-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f3931-123">None</span></span>
<span data-ttu-id="f3931-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f3931-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3931-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3931-125">OUTPUTS</span></span>

### <span data-ttu-id="f3931-126">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımaku</span><span class="sxs-lookup"><span data-stu-id="f3931-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="f3931-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3931-127">NOTES</span></span>

## <span data-ttu-id="f3931-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3931-128">RELATED LINKS</span></span>

[<span data-ttu-id="f3931-129">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="f3931-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f3931-130">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="f3931-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f3931-131">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="f3931-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f3931-132">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="f3931-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


