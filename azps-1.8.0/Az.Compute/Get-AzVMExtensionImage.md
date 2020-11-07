---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ebe1720154c45b08eb84cfe6c1ee4e339859e5fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917427"
---
# <span data-ttu-id="5e69d-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5e69d-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="5e69d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e69d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e69d-103">Bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="5e69d-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="5e69d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e69d-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e69d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e69d-105">DESCRIPTION</span></span>
<span data-ttu-id="5e69d-106">**Get-Azvmextensionımage** cmdlet 'ı bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="5e69d-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="5e69d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e69d-107">EXAMPLES</span></span>

### <span data-ttu-id="5e69d-108">Örnek 1: uzantı resminin sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="5e69d-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="5e69d-109">Bu komut, belirtilen konum, yayıncı ve tür için uzantı resminin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5e69d-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="5e69d-110">Örnek 2: sürüm üzerinde filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="5e69d-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="5e69d-111">Bu komut, 12 ile başlayan belirtilen konum, yayıncı, tür ve sürüm için uzantı görüntüsünün tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5e69d-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="5e69d-112">Örnek 3: sürüm üzerinde filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="5e69d-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="5e69d-113">Bu komut, belirtilen konum, yayıncı, tür ve sürüm için uzantı resminin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5e69d-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="5e69d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e69d-114">PARAMETERS</span></span>

### <span data-ttu-id="5e69d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e69d-115">-DefaultProfile</span></span>
<span data-ttu-id="5e69d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e69d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e69d-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="5e69d-117">-FilterExpression</span></span>
<span data-ttu-id="5e69d-118">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e69d-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69d-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="5e69d-119">-Location</span></span>
<span data-ttu-id="5e69d-120">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e69d-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="5e69d-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5e69d-121">-PublisherName</span></span>
<span data-ttu-id="5e69d-122">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e69d-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="5e69d-123">Uzantı yayımcısı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e69d-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5e69d-124">-Tür</span><span class="sxs-lookup"><span data-stu-id="5e69d-124">-Type</span></span>
<span data-ttu-id="5e69d-125">Uzantının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e69d-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="5e69d-126">Uzantı türü edinmek için Get-AzVMExtensionImageType cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e69d-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="5e69d-127">-Version</span><span class="sxs-lookup"><span data-stu-id="5e69d-127">-Version</span></span>
<span data-ttu-id="5e69d-128">Bu cmdlet 'in aldığı uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e69d-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5e69d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e69d-129">CommonParameters</span></span>
<span data-ttu-id="5e69d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e69d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e69d-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e69d-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e69d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e69d-132">INPUTS</span></span>

### <span data-ttu-id="5e69d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5e69d-133">System.String</span></span>

## <span data-ttu-id="5e69d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e69d-134">OUTPUTS</span></span>

### <span data-ttu-id="5e69d-135">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımage</span><span class="sxs-lookup"><span data-stu-id="5e69d-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="5e69d-136">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineextensionımagedetails</span><span class="sxs-lookup"><span data-stu-id="5e69d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="5e69d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e69d-137">NOTES</span></span>

## <span data-ttu-id="5e69d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e69d-138">RELATED LINKS</span></span>

[<span data-ttu-id="5e69d-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="5e69d-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="5e69d-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5e69d-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="5e69d-141">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="5e69d-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


