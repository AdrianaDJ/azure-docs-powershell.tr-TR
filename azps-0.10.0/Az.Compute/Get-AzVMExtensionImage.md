---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937019"
---
# <span data-ttu-id="d3080-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d3080-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="d3080-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3080-102">SYNOPSIS</span></span>
<span data-ttu-id="d3080-103">Bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="d3080-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="d3080-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3080-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3080-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3080-105">DESCRIPTION</span></span>
<span data-ttu-id="d3080-106">**Get-Azvmextensionımage** cmdlet 'ı bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="d3080-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="d3080-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3080-107">EXAMPLES</span></span>

### <span data-ttu-id="d3080-108">Örnek 1: uzantı resminin sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="d3080-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="d3080-109">Bu komut, belirtilen konum, yayıncı ve tür için uzantı resminin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d3080-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="d3080-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3080-110">PARAMETERS</span></span>

### <span data-ttu-id="d3080-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3080-111">-DefaultProfile</span></span>
<span data-ttu-id="d3080-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3080-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3080-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="d3080-113">-FilterExpression</span></span>
<span data-ttu-id="d3080-114">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3080-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3080-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="d3080-115">-Location</span></span>
<span data-ttu-id="d3080-116">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3080-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="d3080-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d3080-117">-PublisherName</span></span>
<span data-ttu-id="d3080-118">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3080-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="d3080-119">Uzantı yayımcısı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d3080-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d3080-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="d3080-120">-Type</span></span>
<span data-ttu-id="d3080-121">Uzantının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3080-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="d3080-122">Uzantı türü edinmek için Get-AzVMExtensionImageType cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d3080-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="d3080-123">-Version</span><span class="sxs-lookup"><span data-stu-id="d3080-123">-Version</span></span>
<span data-ttu-id="d3080-124">Bu cmdlet 'in aldığı uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3080-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3080-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3080-125">CommonParameters</span></span>
<span data-ttu-id="d3080-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3080-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3080-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3080-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3080-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3080-128">INPUTS</span></span>

### <span data-ttu-id="d3080-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3080-129">None</span></span>
<span data-ttu-id="d3080-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d3080-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3080-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3080-131">OUTPUTS</span></span>

### <span data-ttu-id="d3080-132">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımage</span><span class="sxs-lookup"><span data-stu-id="d3080-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="d3080-133">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımagedetails</span><span class="sxs-lookup"><span data-stu-id="d3080-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="d3080-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3080-134">NOTES</span></span>

## <span data-ttu-id="d3080-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3080-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3080-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="d3080-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="d3080-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d3080-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d3080-138">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="d3080-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


