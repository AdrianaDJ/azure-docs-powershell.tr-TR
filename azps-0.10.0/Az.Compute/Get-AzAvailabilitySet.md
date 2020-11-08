---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: ef42e8910b9ff6a71277c998825aa53cd3ad085e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937059"
---
# <span data-ttu-id="3e7d5-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3e7d5-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="3e7d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7d5-103">Kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="3e7d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e7d5-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e7d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="3e7d5-106">**Get-AzAvailabilitySet** cmdlet 'i kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="3e7d5-107">Alınacak belirli bir kullanılabilirlik kümesinin adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="3e7d5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e7d5-108">EXAMPLES</span></span>

### <span data-ttu-id="3e7d5-109">Örnek 1: belirli bir kullanılabilirlik kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="3e7d5-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="3e7d5-110">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="3e7d5-111">Örnek 2: tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="3e7d5-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3e7d5-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="3e7d5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e7d5-113">PARAMETERS</span></span>

### <span data-ttu-id="3e7d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e7d5-114">-DefaultProfile</span></span>
<span data-ttu-id="3e7d5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e7d5-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e7d5-116">-Name</span></span>
<span data-ttu-id="3e7d5-117">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3e7d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e7d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="3e7d5-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3e7d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7d5-120">CommonParameters</span></span>
<span data-ttu-id="3e7d5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7d5-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e7d5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7d5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e7d5-123">INPUTS</span></span>

### <span data-ttu-id="3e7d5-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3e7d5-124">None</span></span>
<span data-ttu-id="3e7d5-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3e7d5-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e7d5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e7d5-126">OUTPUTS</span></span>

### <span data-ttu-id="3e7d5-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3e7d5-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="3e7d5-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e7d5-128">NOTES</span></span>

## <span data-ttu-id="3e7d5-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e7d5-129">RELATED LINKS</span></span>

[<span data-ttu-id="3e7d5-130">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3e7d5-130">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="3e7d5-131">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3e7d5-131">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)

