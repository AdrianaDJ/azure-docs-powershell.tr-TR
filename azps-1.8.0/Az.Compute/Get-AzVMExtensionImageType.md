---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 0e3c1a9113bf3872ca86227272e36abd67781b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761343"
---
# <span data-ttu-id="7da2d-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7da2d-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="7da2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7da2d-103">Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="7da2d-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="7da2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7da2d-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da2d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7da2d-105">DESCRIPTION</span></span>
<span data-ttu-id="7da2d-106">**Get-Azvmextensionımagetype** cmdlet 'i, bir Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="7da2d-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="7da2d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7da2d-107">EXAMPLES</span></span>

### <span data-ttu-id="7da2d-108">Örnek 1: uzantı resim türünü alma</span><span class="sxs-lookup"><span data-stu-id="7da2d-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="7da2d-109">Bu komut belirtilen yayımcının ve konumun uzantı resim türünü alır.</span><span class="sxs-lookup"><span data-stu-id="7da2d-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="7da2d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7da2d-110">PARAMETERS</span></span>

### <span data-ttu-id="7da2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da2d-111">-DefaultProfile</span></span>
<span data-ttu-id="7da2d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7da2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da2d-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="7da2d-113">-Location</span></span>
<span data-ttu-id="7da2d-114">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da2d-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="7da2d-115">Bu cmdlet, bu parametrenin belirttiği konumda uzantının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="7da2d-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="7da2d-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7da2d-116">-PublisherName</span></span>
<span data-ttu-id="7da2d-117">Bir uzantının yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da2d-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="7da2d-118">Uzantı yayımcısı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da2d-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="7da2d-119">Bu cmdlet, bu parametrenin belirttiği yayımcının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="7da2d-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="7da2d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da2d-120">CommonParameters</span></span>
<span data-ttu-id="7da2d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7da2d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da2d-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7da2d-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da2d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7da2d-123">INPUTS</span></span>

### <span data-ttu-id="7da2d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7da2d-124">System.String</span></span>

## <span data-ttu-id="7da2d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7da2d-125">OUTPUTS</span></span>

### <span data-ttu-id="7da2d-126">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="7da2d-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="7da2d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7da2d-127">NOTES</span></span>

## <span data-ttu-id="7da2d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7da2d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7da2d-129">Get-Azvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="7da2d-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="7da2d-130">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="7da2d-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


