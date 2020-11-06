---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 45accc1c3fd52720d3764a9167f6354316a0c9fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588265"
---
# <span data-ttu-id="1a90e-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1a90e-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="1a90e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a90e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a90e-103">Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="1a90e-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a90e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a90e-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a90e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a90e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a90e-106">**Get-Azurermvmextensionımagetype** cmdlet 'i, bir Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="1a90e-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="1a90e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a90e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a90e-108">Örnek 1: uzantı resim türünü alma</span><span class="sxs-lookup"><span data-stu-id="1a90e-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="1a90e-109">Bu komut belirtilen yayımcının ve konumun uzantı resim türünü alır.</span><span class="sxs-lookup"><span data-stu-id="1a90e-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="1a90e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a90e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a90e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a90e-111">-DefaultProfile</span></span>
<span data-ttu-id="1a90e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a90e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a90e-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="1a90e-113">-Location</span></span>
<span data-ttu-id="1a90e-114">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a90e-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="1a90e-115">Bu cmdlet, bu parametrenin belirttiği konumda uzantının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="1a90e-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a90e-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1a90e-116">-PublisherName</span></span>
<span data-ttu-id="1a90e-117">Bir uzantının yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a90e-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="1a90e-118">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a90e-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="1a90e-119">Bu cmdlet, bu parametrenin belirttiği yayımcının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="1a90e-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a90e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a90e-120">CommonParameters</span></span>
<span data-ttu-id="1a90e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a90e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a90e-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a90e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a90e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a90e-123">INPUTS</span></span>

## <span data-ttu-id="1a90e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a90e-124">OUTPUTS</span></span>

## <span data-ttu-id="1a90e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a90e-125">NOTES</span></span>

## <span data-ttu-id="1a90e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a90e-126">RELATED LINKS</span></span>

[<span data-ttu-id="1a90e-127">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="1a90e-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="1a90e-128">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="1a90e-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


