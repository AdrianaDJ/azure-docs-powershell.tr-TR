---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752896"
---
# <span data-ttu-id="91eec-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="91eec-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="91eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91eec-102">SYNOPSIS</span></span>
<span data-ttu-id="91eec-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="91eec-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="91eec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91eec-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91eec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91eec-105">DESCRIPTION</span></span>
<span data-ttu-id="91eec-106">**Get-AzVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="91eec-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="91eec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91eec-107">EXAMPLES</span></span>

### <span data-ttu-id="91eec-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="91eec-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="91eec-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="91eec-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="91eec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91eec-110">PARAMETERS</span></span>

### <span data-ttu-id="91eec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91eec-111">-DefaultProfile</span></span>
<span data-ttu-id="91eec-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91eec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91eec-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="91eec-113">-Location</span></span>
<span data-ttu-id="91eec-114">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="91eec-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="91eec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91eec-115">CommonParameters</span></span>
<span data-ttu-id="91eec-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91eec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91eec-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91eec-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91eec-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91eec-118">INPUTS</span></span>

### <span data-ttu-id="91eec-119">System. String</span><span class="sxs-lookup"><span data-stu-id="91eec-119">System.String</span></span>

## <span data-ttu-id="91eec-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91eec-120">OUTPUTS</span></span>

### <span data-ttu-id="91eec-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSUsage</span><span class="sxs-lookup"><span data-stu-id="91eec-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="91eec-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91eec-122">NOTES</span></span>

## <span data-ttu-id="91eec-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91eec-123">RELATED LINKS</span></span>

[<span data-ttu-id="91eec-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="91eec-124">Get-AzVM</span></span>](./Get-AzVM.md)


