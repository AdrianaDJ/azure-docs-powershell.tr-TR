---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591075"
---
# <span data-ttu-id="1f136-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f136-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="1f136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f136-102">SYNOPSIS</span></span>
<span data-ttu-id="1f136-103">Kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1f136-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f136-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f136-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1f136-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f136-105">DESCRIPTION</span></span>
<span data-ttu-id="1f136-106">**Get-AzureRmAvailabilitySet** cmdlet 'i, kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1f136-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="1f136-107">Alınacak belirli bir kullanılabilirlik kümesinin adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f136-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="1f136-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f136-108">EXAMPLES</span></span>

### <span data-ttu-id="1f136-109">Örnek 1: belirli bir kullanılabilirlik kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="1f136-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="1f136-110">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="1f136-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="1f136-111">Örnek 2: tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="1f136-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1f136-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1f136-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1f136-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f136-113">PARAMETERS</span></span>

### <span data-ttu-id="1f136-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f136-114">-Name</span></span>
<span data-ttu-id="1f136-115">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f136-115">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f136-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f136-116">-ResourceGroupName</span></span>
<span data-ttu-id="1f136-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f136-117">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f136-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f136-118">CommonParameters</span></span>
<span data-ttu-id="1f136-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f136-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f136-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f136-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f136-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f136-121">INPUTS</span></span>

### <span data-ttu-id="1f136-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f136-122">None</span></span>
<span data-ttu-id="1f136-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1f136-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f136-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f136-124">OUTPUTS</span></span>

## <span data-ttu-id="1f136-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f136-125">NOTES</span></span>

## <span data-ttu-id="1f136-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f136-126">RELATED LINKS</span></span>

[<span data-ttu-id="1f136-127">Yeni-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f136-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="1f136-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f136-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


