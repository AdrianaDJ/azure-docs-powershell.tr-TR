---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 685dafeb72693a617ca627aa1abcae19c5e24389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588574"
---
# <span data-ttu-id="f45cd-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f45cd-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="f45cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f45cd-103">Kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f45cd-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f45cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f45cd-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f45cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f45cd-106">**Get-AzureRmAvailabilitySet** cmdlet 'i, kaynak grubundaki Azure kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f45cd-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="f45cd-107">Alınacak belirli bir kullanılabilirlik kümesinin adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f45cd-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="f45cd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f45cd-108">EXAMPLES</span></span>

### <span data-ttu-id="f45cd-109">Örnek 1: belirli bir kullanılabilirlik kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="f45cd-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="f45cd-110">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="f45cd-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f45cd-111">Örnek 2: tüm kullanılabilirlik kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="f45cd-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f45cd-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki tüm kullanılabilirlik kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f45cd-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f45cd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f45cd-113">PARAMETERS</span></span>

### <span data-ttu-id="f45cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45cd-114">-DefaultProfile</span></span>
<span data-ttu-id="f45cd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f45cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f45cd-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f45cd-116">-Name</span></span>
<span data-ttu-id="f45cd-117">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f45cd-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="f45cd-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f45cd-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45cd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45cd-120">CommonParameters</span></span>
<span data-ttu-id="f45cd-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f45cd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45cd-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45cd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45cd-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f45cd-123">INPUTS</span></span>

### <span data-ttu-id="f45cd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f45cd-124">System.String</span></span>

## <span data-ttu-id="f45cd-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f45cd-125">OUTPUTS</span></span>

### <span data-ttu-id="f45cd-126">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f45cd-126">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f45cd-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f45cd-127">NOTES</span></span>

## <span data-ttu-id="f45cd-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f45cd-128">RELATED LINKS</span></span>

[<span data-ttu-id="f45cd-129">Yeni-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f45cd-129">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="f45cd-130">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f45cd-130">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


