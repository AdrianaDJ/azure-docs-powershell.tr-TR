---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: eb56542d02498a0d4b8aa4176c77d75ab6ad4da6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937013"
---
# <span data-ttu-id="3b8ee-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3b8ee-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="3b8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8ee-103">Vmımage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="3b8ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b8ee-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b8ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b8ee-105">DESCRIPTION</span></span>
<span data-ttu-id="3b8ee-106">**Get-Azvmimageteklifini** , VMImage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="3b8ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b8ee-107">EXAMPLES</span></span>

### <span data-ttu-id="3b8ee-108">Örnek 1: Yayımcı için teklif türleri alma</span><span class="sxs-lookup"><span data-stu-id="3b8ee-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="3b8ee-109">Bu komut, Merkezi ABD bölgesindeki Belirtilen yayımcının teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="3b8ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b8ee-110">PARAMETERS</span></span>

### <span data-ttu-id="3b8ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8ee-111">-DefaultProfile</span></span>
<span data-ttu-id="3b8ee-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b8ee-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="3b8ee-113">-Location</span></span>
<span data-ttu-id="3b8ee-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3b8ee-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3b8ee-115">-PublisherName</span></span>
<span data-ttu-id="3b8ee-116">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="3b8ee-117">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="3b8ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8ee-118">CommonParameters</span></span>
<span data-ttu-id="3b8ee-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8ee-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8ee-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8ee-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b8ee-121">INPUTS</span></span>

### <span data-ttu-id="3b8ee-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3b8ee-122">None</span></span>
<span data-ttu-id="3b8ee-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3b8ee-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b8ee-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b8ee-124">OUTPUTS</span></span>

### <span data-ttu-id="3b8ee-125">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımageteklifini</span><span class="sxs-lookup"><span data-stu-id="3b8ee-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="3b8ee-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b8ee-126">NOTES</span></span>

## <span data-ttu-id="3b8ee-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b8ee-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b8ee-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3b8ee-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3b8ee-129">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="3b8ee-129">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3b8ee-130">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3b8ee-130">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="3b8ee-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3b8ee-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


