---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 80fc102c31e4019576a6f2c65ee1c93e19b81590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759801"
---
# <span data-ttu-id="f49bd-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f49bd-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f49bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f49bd-103">PowerBI Embedded kapasitesi örneğinin varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="f49bd-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f49bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f49bd-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f49bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f49bd-105">DESCRIPTION</span></span>
<span data-ttu-id="f49bd-106">Test-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesi örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="f49bd-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f49bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f49bd-107">EXAMPLES</span></span>

### <span data-ttu-id="f49bd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f49bd-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="f49bd-109">Bu komut, test</span><span class="sxs-lookup"><span data-stu-id="f49bd-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="f49bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f49bd-110">PARAMETERS</span></span>

### <span data-ttu-id="f49bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49bd-111">-DefaultProfile</span></span>
<span data-ttu-id="f49bd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f49bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49bd-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f49bd-113">-Name</span></span>
<span data-ttu-id="f49bd-114">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="f49bd-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="f49bd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49bd-115">CommonParameters</span></span>
<span data-ttu-id="f49bd-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f49bd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49bd-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49bd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49bd-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f49bd-118">INPUTS</span></span>

### <span data-ttu-id="f49bd-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f49bd-119">None</span></span>

## <span data-ttu-id="f49bd-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f49bd-120">OUTPUTS</span></span>

### <span data-ttu-id="f49bd-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f49bd-121">System.Boolean</span></span>

## <span data-ttu-id="f49bd-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f49bd-122">NOTES</span></span>

## <span data-ttu-id="f49bd-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f49bd-123">RELATED LINKS</span></span>

[<span data-ttu-id="f49bd-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f49bd-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f49bd-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f49bd-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
