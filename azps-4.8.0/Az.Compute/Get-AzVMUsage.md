---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108127"
---
# <span data-ttu-id="c1a4d-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="c1a4d-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="c1a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a4d-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c1a4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1a4d-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a4d-106">**Get-AzVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c1a4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="c1a4d-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="c1a4d-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="c1a4d-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="c1a4d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1a4d-110">PARAMETERS</span></span>

### <span data-ttu-id="c1a4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a4d-111">-DefaultProfile</span></span>
<span data-ttu-id="c1a4d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1a4d-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="c1a4d-113">-Location</span></span>
<span data-ttu-id="c1a4d-114">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a4d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a4d-115">CommonParameters</span></span>
<span data-ttu-id="c1a4d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a4d-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1a4d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a4d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1a4d-118">INPUTS</span></span>

### <span data-ttu-id="c1a4d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c1a4d-119">System.String</span></span>

## <span data-ttu-id="c1a4d-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1a4d-120">OUTPUTS</span></span>

### <span data-ttu-id="c1a4d-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSUsage</span><span class="sxs-lookup"><span data-stu-id="c1a4d-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="c1a4d-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1a4d-122">NOTES</span></span>

## <span data-ttu-id="c1a4d-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1a4d-123">RELATED LINKS</span></span>

[<span data-ttu-id="c1a4d-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c1a4d-124">Get-AzVM</span></span>](./Get-AzVM.md)


