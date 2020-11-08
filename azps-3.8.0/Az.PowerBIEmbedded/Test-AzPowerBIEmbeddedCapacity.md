---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095811"
---
# <span data-ttu-id="10099-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="10099-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="10099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10099-102">SYNOPSIS</span></span>
<span data-ttu-id="10099-103">PowerBI Embedded kapasitesi örneğinin varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="10099-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="10099-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10099-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10099-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10099-105">DESCRIPTION</span></span>
<span data-ttu-id="10099-106">Test-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesi örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="10099-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="10099-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10099-107">EXAMPLES</span></span>

### <span data-ttu-id="10099-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10099-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="10099-109">Bu komut, test</span><span class="sxs-lookup"><span data-stu-id="10099-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="10099-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10099-110">PARAMETERS</span></span>

### <span data-ttu-id="10099-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10099-111">-DefaultProfile</span></span>
<span data-ttu-id="10099-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10099-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10099-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="10099-113">-Name</span></span>
<span data-ttu-id="10099-114">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="10099-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="10099-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10099-115">CommonParameters</span></span>
<span data-ttu-id="10099-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10099-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10099-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10099-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10099-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10099-118">INPUTS</span></span>

### <span data-ttu-id="10099-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="10099-119">None</span></span>

## <span data-ttu-id="10099-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10099-120">OUTPUTS</span></span>

### <span data-ttu-id="10099-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10099-121">System.Boolean</span></span>

## <span data-ttu-id="10099-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10099-122">NOTES</span></span>

## <span data-ttu-id="10099-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10099-123">RELATED LINKS</span></span>

[<span data-ttu-id="10099-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="10099-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="10099-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="10099-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
