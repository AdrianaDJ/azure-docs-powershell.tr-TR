---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762910"
---
# <span data-ttu-id="f5a88-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f5a88-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f5a88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a88-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a88-103">PowerBI Embedded kapasitesi örneğinin varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="f5a88-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5a88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5a88-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5a88-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5a88-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a88-106">Test-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesi örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="f5a88-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f5a88-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5a88-107">EXAMPLES</span></span>

### <span data-ttu-id="f5a88-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5a88-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="f5a88-109">Bu komut, test</span><span class="sxs-lookup"><span data-stu-id="f5a88-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="f5a88-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5a88-110">PARAMETERS</span></span>

### <span data-ttu-id="f5a88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a88-111">-DefaultProfile</span></span>
<span data-ttu-id="f5a88-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5a88-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a88-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5a88-113">-Name</span></span>
<span data-ttu-id="f5a88-114">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="f5a88-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a88-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a88-115">CommonParameters</span></span>
<span data-ttu-id="f5a88-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5a88-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a88-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a88-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a88-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5a88-118">INPUTS</span></span>

### <span data-ttu-id="f5a88-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f5a88-119">None</span></span>

## <span data-ttu-id="f5a88-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5a88-120">OUTPUTS</span></span>

### <span data-ttu-id="f5a88-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5a88-121">System.Boolean</span></span>

## <span data-ttu-id="f5a88-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5a88-122">NOTES</span></span>

## <span data-ttu-id="f5a88-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5a88-123">RELATED LINKS</span></span>

[<span data-ttu-id="f5a88-124">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="f5a88-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f5a88-125">Remove-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="f5a88-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
