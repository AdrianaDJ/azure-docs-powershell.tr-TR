---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573393"
---
# <span data-ttu-id="6a879-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6a879-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6a879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a879-102">SYNOPSIS</span></span>
<span data-ttu-id="6a879-103">PowerBI Embedded kapasitesi örneğinin varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="6a879-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a879-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a879-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="6a879-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a879-105">DESCRIPTION</span></span>
<span data-ttu-id="6a879-106">Test-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesi örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="6a879-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="6a879-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a879-107">EXAMPLES</span></span>

### <span data-ttu-id="6a879-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a879-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="6a879-109">Bu komut, test</span><span class="sxs-lookup"><span data-stu-id="6a879-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="6a879-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a879-110">PARAMETERS</span></span>

### <span data-ttu-id="6a879-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a879-111">-Name</span></span>
<span data-ttu-id="6a879-112">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="6a879-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="6a879-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a879-113">CommonParameters</span></span>
<span data-ttu-id="6a879-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a879-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a879-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a879-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a879-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a879-116">INPUTS</span></span>

### <span data-ttu-id="6a879-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6a879-117">None</span></span>
<span data-ttu-id="6a879-118">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6a879-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a879-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a879-119">OUTPUTS</span></span>

### <span data-ttu-id="6a879-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a879-120">System.Boolean</span></span>

## <span data-ttu-id="6a879-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a879-121">NOTES</span></span>

## <span data-ttu-id="6a879-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a879-122">RELATED LINKS</span></span>

[<span data-ttu-id="6a879-123">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="6a879-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="6a879-124">Remove-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="6a879-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
