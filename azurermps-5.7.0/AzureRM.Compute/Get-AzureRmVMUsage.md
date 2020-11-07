---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764475"
---
# <span data-ttu-id="14b32-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="14b32-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="14b32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b32-102">SYNOPSIS</span></span>
<span data-ttu-id="14b32-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="14b32-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14b32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14b32-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="14b32-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14b32-105">DESCRIPTION</span></span>
<span data-ttu-id="14b32-106">**Get-AzureRmVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="14b32-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="14b32-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14b32-107">EXAMPLES</span></span>

### <span data-ttu-id="14b32-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="14b32-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="14b32-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="14b32-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="14b32-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14b32-110">PARAMETERS</span></span>

### <span data-ttu-id="14b32-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="14b32-111">-Location</span></span>
<span data-ttu-id="14b32-112">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="14b32-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="14b32-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b32-113">CommonParameters</span></span>
<span data-ttu-id="14b32-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14b32-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b32-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b32-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b32-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14b32-116">INPUTS</span></span>

### <span data-ttu-id="14b32-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14b32-117">None</span></span>
<span data-ttu-id="14b32-118">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="14b32-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14b32-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14b32-119">OUTPUTS</span></span>

## <span data-ttu-id="14b32-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14b32-120">NOTES</span></span>

## <span data-ttu-id="14b32-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14b32-121">RELATED LINKS</span></span>

[<span data-ttu-id="14b32-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="14b32-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


