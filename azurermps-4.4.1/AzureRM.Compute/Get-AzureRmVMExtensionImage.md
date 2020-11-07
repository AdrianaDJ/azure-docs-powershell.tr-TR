---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 7010808e1879566d3b0fc78f82d0e9f82bdd626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763399"
---
# <span data-ttu-id="4ed34-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4ed34-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="4ed34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed34-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed34-103">Bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="4ed34-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ed34-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ed34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ed34-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed34-106">**Get-Azurermvmextensionımage** cmdlet 'ı bir Azure uzantısı için tüm sürümleri alır.</span><span class="sxs-lookup"><span data-stu-id="4ed34-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="4ed34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ed34-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed34-108">Örnek 1: uzantı resminin sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="4ed34-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="4ed34-109">Bu komut, belirtilen konum, yayıncı ve tür için uzantı resminin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4ed34-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="4ed34-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ed34-110">PARAMETERS</span></span>

### <span data-ttu-id="4ed34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed34-111">-DefaultProfile</span></span>
<span data-ttu-id="4ed34-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ed34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed34-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="4ed34-113">-FilterExpression</span></span>
<span data-ttu-id="4ed34-114">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed34-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="4ed34-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="4ed34-115">-Location</span></span>
<span data-ttu-id="4ed34-116">Bir uzantının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed34-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="4ed34-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4ed34-117">-PublisherName</span></span>
<span data-ttu-id="4ed34-118">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed34-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="4ed34-119">Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4ed34-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4ed34-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="4ed34-120">-Type</span></span>
<span data-ttu-id="4ed34-121">Uzantının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed34-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="4ed34-122">Uzantı türü edinmek için Get-AzureRmVMExtensionImageType cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4ed34-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="4ed34-123">-Version</span><span class="sxs-lookup"><span data-stu-id="4ed34-123">-Version</span></span>
<span data-ttu-id="4ed34-124">Bu cmdlet 'in aldığı uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed34-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed34-125">CommonParameters</span></span>
<span data-ttu-id="4ed34-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ed34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed34-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed34-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed34-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ed34-128">INPUTS</span></span>

## <span data-ttu-id="4ed34-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ed34-129">OUTPUTS</span></span>

## <span data-ttu-id="4ed34-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ed34-130">NOTES</span></span>

## <span data-ttu-id="4ed34-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ed34-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ed34-132">Get-Azurermvmextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="4ed34-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="4ed34-133">Get-Azurermvmımage</span><span class="sxs-lookup"><span data-stu-id="4ed34-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4ed34-134">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4ed34-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


