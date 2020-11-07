---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
ms.openlocfilehash: ccb48064bb2d6b91801a58ecfa9d229a748889a8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939423"
---
# <span data-ttu-id="4550a-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4550a-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="4550a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4550a-102">SYNOPSIS</span></span>
<span data-ttu-id="4550a-103">Bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="4550a-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4550a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4550a-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4550a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4550a-105">DESCRIPTION</span></span>
<span data-ttu-id="4550a-106">**Get-Azurermvmextensionımage** cmdlet 'ı bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="4550a-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="4550a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4550a-107">EXAMPLES</span></span>

### <span data-ttu-id="4550a-108">Örnek 1: uzantı resminin sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="4550a-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="4550a-109">Bu komut, belirtilen konum, yayıncı ve tür için uzantı resminin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4550a-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="4550a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4550a-110">PARAMETERS</span></span>

### <span data-ttu-id="4550a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4550a-111">-DefaultProfile</span></span>
<span data-ttu-id="4550a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4550a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4550a-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="4550a-113">-FilterExpression</span></span>
<span data-ttu-id="4550a-114">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4550a-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="4550a-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="4550a-115">-Location</span></span>
<span data-ttu-id="4550a-116">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4550a-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="4550a-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4550a-117">-PublisherName</span></span>
<span data-ttu-id="4550a-118">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4550a-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="4550a-119">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4550a-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4550a-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="4550a-120">-Type</span></span>
<span data-ttu-id="4550a-121">Uzantının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4550a-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="4550a-122">Uzantı türü edinmek için Get-AzureRmVMExtensionImageType cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4550a-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="4550a-123">-Version</span><span class="sxs-lookup"><span data-stu-id="4550a-123">-Version</span></span>
<span data-ttu-id="4550a-124">Bu cmdlet 'in aldığı uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4550a-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4550a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4550a-125">CommonParameters</span></span>
<span data-ttu-id="4550a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4550a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4550a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4550a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4550a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4550a-128">INPUTS</span></span>

### <span data-ttu-id="4550a-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4550a-129">None</span></span>
<span data-ttu-id="4550a-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4550a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4550a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4550a-131">OUTPUTS</span></span>

### <span data-ttu-id="4550a-132">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımage</span><span class="sxs-lookup"><span data-stu-id="4550a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="4550a-133">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımagedetails</span><span class="sxs-lookup"><span data-stu-id="4550a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="4550a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4550a-134">NOTES</span></span>

## <span data-ttu-id="4550a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4550a-135">RELATED LINKS</span></span>

[<span data-ttu-id="4550a-136">Get-Azurermvmextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="4550a-136">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="4550a-137">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="4550a-137">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4550a-138">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4550a-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


