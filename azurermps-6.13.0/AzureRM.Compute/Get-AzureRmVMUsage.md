---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 22f77bfc5802527103dd0e391a11e16833696abd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592052"
---
# <span data-ttu-id="215cb-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="215cb-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="215cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="215cb-102">SYNOPSIS</span></span>
<span data-ttu-id="215cb-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="215cb-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="215cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="215cb-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="215cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="215cb-105">DESCRIPTION</span></span>
<span data-ttu-id="215cb-106">**Get-AzureRmVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="215cb-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="215cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="215cb-107">EXAMPLES</span></span>

### <span data-ttu-id="215cb-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="215cb-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="215cb-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="215cb-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="215cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="215cb-110">PARAMETERS</span></span>

### <span data-ttu-id="215cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215cb-111">-DefaultProfile</span></span>
<span data-ttu-id="215cb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="215cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="215cb-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="215cb-113">-Location</span></span>
<span data-ttu-id="215cb-114">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="215cb-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="215cb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215cb-115">CommonParameters</span></span>
<span data-ttu-id="215cb-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="215cb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215cb-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="215cb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215cb-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="215cb-118">INPUTS</span></span>

### <span data-ttu-id="215cb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="215cb-119">System.String</span></span>

## <span data-ttu-id="215cb-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="215cb-120">OUTPUTS</span></span>

### <span data-ttu-id="215cb-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSUsage</span><span class="sxs-lookup"><span data-stu-id="215cb-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="215cb-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="215cb-122">NOTES</span></span>

## <span data-ttu-id="215cb-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="215cb-123">RELATED LINKS</span></span>

[<span data-ttu-id="215cb-124">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="215cb-124">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


