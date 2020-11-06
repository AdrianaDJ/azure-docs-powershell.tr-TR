---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590961"
---
# <span data-ttu-id="88647-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="88647-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="88647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88647-102">SYNOPSIS</span></span>
<span data-ttu-id="88647-103">Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="88647-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88647-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88647-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88647-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88647-105">DESCRIPTION</span></span>
<span data-ttu-id="88647-106">**Get-Azurermvmextensionımagetype** cmdlet 'i, bir Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="88647-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="88647-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88647-107">EXAMPLES</span></span>

### <span data-ttu-id="88647-108">Örnek 1: uzantı resim türünü alma</span><span class="sxs-lookup"><span data-stu-id="88647-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="88647-109">Bu komut belirtilen yayımcının ve konumun uzantı resim türünü alır.</span><span class="sxs-lookup"><span data-stu-id="88647-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="88647-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88647-110">PARAMETERS</span></span>

### <span data-ttu-id="88647-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88647-111">-DefaultProfile</span></span>
<span data-ttu-id="88647-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88647-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88647-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="88647-113">-Location</span></span>
<span data-ttu-id="88647-114">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="88647-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="88647-115">Bu cmdlet, bu parametrenin belirttiği konumda uzantının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="88647-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="88647-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="88647-116">-PublisherName</span></span>
<span data-ttu-id="88647-117">Bir uzantının yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88647-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="88647-118">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="88647-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="88647-119">Bu cmdlet, bu parametrenin belirttiği yayımcının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="88647-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="88647-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88647-120">CommonParameters</span></span>
<span data-ttu-id="88647-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88647-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88647-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88647-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88647-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88647-123">INPUTS</span></span>

### <span data-ttu-id="88647-124">System. String</span><span class="sxs-lookup"><span data-stu-id="88647-124">System.String</span></span>

## <span data-ttu-id="88647-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88647-125">OUTPUTS</span></span>

### <span data-ttu-id="88647-126">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="88647-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="88647-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88647-127">NOTES</span></span>

## <span data-ttu-id="88647-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88647-128">RELATED LINKS</span></span>

[<span data-ttu-id="88647-129">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="88647-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="88647-130">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="88647-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


