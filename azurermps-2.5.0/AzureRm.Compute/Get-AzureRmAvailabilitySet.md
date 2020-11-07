---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938992"
---
# <span data-ttu-id="a97c8-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a97c8-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="a97c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a97c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a97c8-103">Kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a97c8-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a97c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a97c8-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a97c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a97c8-105">DESCRIPTION</span></span>
<span data-ttu-id="a97c8-106">**Get-AzureRmAvailabilitySet** cmdlet 'i, kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a97c8-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="a97c8-107">Alınacak belirli bir kullanılabilirlik kümesinin adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a97c8-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="a97c8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a97c8-108">EXAMPLES</span></span>

### <span data-ttu-id="a97c8-109">Örnek 1: belirli bir kullanılabilirlik kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="a97c8-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="a97c8-110">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="a97c8-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="a97c8-111">Örnek 2: tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="a97c8-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a97c8-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a97c8-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a97c8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a97c8-113">PARAMETERS</span></span>

### <span data-ttu-id="a97c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97c8-114">-DefaultProfile</span></span>
<span data-ttu-id="a97c8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a97c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a97c8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a97c8-116">-Name</span></span>
<span data-ttu-id="a97c8-117">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a97c8-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a97c8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97c8-118">-ResourceGroupName</span></span>
<span data-ttu-id="a97c8-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a97c8-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a97c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97c8-120">CommonParameters</span></span>
<span data-ttu-id="a97c8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a97c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97c8-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a97c8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97c8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a97c8-123">INPUTS</span></span>

### <span data-ttu-id="a97c8-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a97c8-124">None</span></span>
<span data-ttu-id="a97c8-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a97c8-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a97c8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a97c8-126">OUTPUTS</span></span>

### <span data-ttu-id="a97c8-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a97c8-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="a97c8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a97c8-128">NOTES</span></span>

## <span data-ttu-id="a97c8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a97c8-129">RELATED LINKS</span></span>

[<span data-ttu-id="a97c8-130">Yeni-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a97c8-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="a97c8-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a97c8-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


