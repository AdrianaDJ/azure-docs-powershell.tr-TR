---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939421"
---
# <span data-ttu-id="bc6d0-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="bc6d0-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="bc6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6d0-103">Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc6d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc6d0-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc6d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6d0-106">**Get-Azurermvmextensionımagetype** cmdlet 'i, bir Azure uzantısının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="bc6d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc6d0-107">EXAMPLES</span></span>

### <span data-ttu-id="bc6d0-108">Örnek 1: uzantı resim türünü alma</span><span class="sxs-lookup"><span data-stu-id="bc6d0-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="bc6d0-109">Bu komut belirtilen yayımcının ve konumun uzantı resim türünü alır.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="bc6d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc6d0-110">PARAMETERS</span></span>

### <span data-ttu-id="bc6d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6d0-111">-DefaultProfile</span></span>
<span data-ttu-id="bc6d0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc6d0-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="bc6d0-113">-Location</span></span>
<span data-ttu-id="bc6d0-114">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="bc6d0-115">Bu cmdlet, bu parametrenin belirttiği konumda uzantının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc6d0-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="bc6d0-116">-PublisherName</span></span>
<span data-ttu-id="bc6d0-117">Bir uzantının yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="bc6d0-118">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="bc6d0-119">Bu cmdlet, bu parametrenin belirttiği yayımcının türünü alır.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc6d0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6d0-120">CommonParameters</span></span>
<span data-ttu-id="bc6d0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6d0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6d0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6d0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc6d0-123">INPUTS</span></span>

### <span data-ttu-id="bc6d0-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc6d0-124">None</span></span>
<span data-ttu-id="bc6d0-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bc6d0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc6d0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc6d0-126">OUTPUTS</span></span>

### <span data-ttu-id="bc6d0-127">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="bc6d0-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="bc6d0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc6d0-128">NOTES</span></span>

## <span data-ttu-id="bc6d0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc6d0-129">RELATED LINKS</span></span>

[<span data-ttu-id="bc6d0-130">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="bc6d0-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="bc6d0-131">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="bc6d0-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


