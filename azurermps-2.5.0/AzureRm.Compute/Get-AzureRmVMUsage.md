---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940188"
---
# <span data-ttu-id="88e0d-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="88e0d-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="88e0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="88e0d-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="88e0d-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88e0d-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88e0d-105">DESCRIPTION</span></span>
<span data-ttu-id="88e0d-106">**Get-AzureRmVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="88e0d-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="88e0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88e0d-107">EXAMPLES</span></span>

### <span data-ttu-id="88e0d-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="88e0d-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="88e0d-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="88e0d-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="88e0d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88e0d-110">PARAMETERS</span></span>

### <span data-ttu-id="88e0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e0d-111">-DefaultProfile</span></span>
<span data-ttu-id="88e0d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88e0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88e0d-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="88e0d-113">-Location</span></span>
<span data-ttu-id="88e0d-114">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="88e0d-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="88e0d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e0d-115">CommonParameters</span></span>
<span data-ttu-id="88e0d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88e0d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e0d-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e0d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e0d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88e0d-118">INPUTS</span></span>

### <span data-ttu-id="88e0d-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="88e0d-119">None</span></span>
<span data-ttu-id="88e0d-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="88e0d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88e0d-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88e0d-121">OUTPUTS</span></span>

### <span data-ttu-id="88e0d-122">Microsoft. Azure. Commands. COMPUTE. modeller. PSUsage</span><span class="sxs-lookup"><span data-stu-id="88e0d-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="88e0d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88e0d-123">NOTES</span></span>

## <span data-ttu-id="88e0d-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88e0d-124">RELATED LINKS</span></span>

[<span data-ttu-id="88e0d-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88e0d-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


