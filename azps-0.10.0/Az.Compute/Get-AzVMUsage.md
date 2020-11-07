---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937000"
---
# <span data-ttu-id="7f79d-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="7f79d-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="7f79d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f79d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f79d-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="7f79d-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="7f79d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f79d-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f79d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f79d-105">DESCRIPTION</span></span>
<span data-ttu-id="7f79d-106">**Get-AzVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="7f79d-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="7f79d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f79d-107">EXAMPLES</span></span>

### <span data-ttu-id="7f79d-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="7f79d-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="7f79d-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="7f79d-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="7f79d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f79d-110">PARAMETERS</span></span>

### <span data-ttu-id="7f79d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f79d-111">-DefaultProfile</span></span>
<span data-ttu-id="7f79d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f79d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f79d-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="7f79d-113">-Location</span></span>
<span data-ttu-id="7f79d-114">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f79d-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="7f79d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f79d-115">CommonParameters</span></span>
<span data-ttu-id="7f79d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f79d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f79d-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f79d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f79d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f79d-118">INPUTS</span></span>

### <span data-ttu-id="7f79d-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f79d-119">None</span></span>
<span data-ttu-id="7f79d-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7f79d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f79d-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f79d-121">OUTPUTS</span></span>

### <span data-ttu-id="7f79d-122">Microsoft. Azure. Commands. COMPUTE. modeller. PSUsage</span><span class="sxs-lookup"><span data-stu-id="7f79d-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="7f79d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f79d-123">NOTES</span></span>

## <span data-ttu-id="7f79d-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f79d-124">RELATED LINKS</span></span>

[<span data-ttu-id="7f79d-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f79d-125">Get-AzVM</span></span>](./Get-AzVM.md)


