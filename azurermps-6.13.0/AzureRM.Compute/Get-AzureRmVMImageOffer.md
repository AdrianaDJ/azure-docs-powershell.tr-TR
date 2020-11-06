---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: 66c0355af202c5900fddc60c81e92f2851ddc1ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590957"
---
# <span data-ttu-id="5d210-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="5d210-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="5d210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d210-102">SYNOPSIS</span></span>
<span data-ttu-id="5d210-103">Vmımage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d210-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d210-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d210-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d210-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d210-105">DESCRIPTION</span></span>
<span data-ttu-id="5d210-106">**Get-Azurermvmımageteklifini** , VMImage teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d210-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="5d210-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d210-107">EXAMPLES</span></span>

### <span data-ttu-id="5d210-108">Örnek 1: Yayımcı için teklif türleri alma</span><span class="sxs-lookup"><span data-stu-id="5d210-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="5d210-109">Bu komut, Merkezi ABD bölgesindeki Belirtilen yayımcının teklif türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d210-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="5d210-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d210-110">PARAMETERS</span></span>

### <span data-ttu-id="5d210-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d210-111">-DefaultProfile</span></span>
<span data-ttu-id="5d210-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d210-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d210-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="5d210-113">-Location</span></span>
<span data-ttu-id="5d210-114">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d210-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="5d210-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5d210-115">-PublisherName</span></span>
<span data-ttu-id="5d210-116">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d210-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="5d210-117">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5d210-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5d210-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d210-118">CommonParameters</span></span>
<span data-ttu-id="5d210-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d210-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d210-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d210-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d210-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d210-121">INPUTS</span></span>

### <span data-ttu-id="5d210-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5d210-122">System.String</span></span>

## <span data-ttu-id="5d210-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d210-123">OUTPUTS</span></span>

### <span data-ttu-id="5d210-124">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımageteklifini</span><span class="sxs-lookup"><span data-stu-id="5d210-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="5d210-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d210-125">NOTES</span></span>

## <span data-ttu-id="5d210-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d210-126">RELATED LINKS</span></span>

[<span data-ttu-id="5d210-127">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="5d210-127">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="5d210-128">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="5d210-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5d210-129">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5d210-129">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="5d210-130">Save-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="5d210-130">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


