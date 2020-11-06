---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592641"
---
# <span data-ttu-id="33861-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="33861-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="33861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33861-102">SYNOPSIS</span></span>
<span data-ttu-id="33861-103">Bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="33861-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33861-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33861-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33861-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33861-105">DESCRIPTION</span></span>
<span data-ttu-id="33861-106">**Get-AzureRmVMUsage** cmdlet 'i, bir konum için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="33861-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="33861-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33861-107">EXAMPLES</span></span>

### <span data-ttu-id="33861-108">Örnek 1: bir konum için çekirdek sayısı kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="33861-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="33861-109">Bu komut, konum Merkezi için sanal makine çekirdek sayısı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="33861-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="33861-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33861-110">PARAMETERS</span></span>

### <span data-ttu-id="33861-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33861-111">-DefaultProfile</span></span>
<span data-ttu-id="33861-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33861-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33861-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="33861-113">-Location</span></span>
<span data-ttu-id="33861-114">Bu cmdlet 'in sanal makine çekirdek sayısı kullanımını aldığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="33861-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="33861-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33861-115">CommonParameters</span></span>
<span data-ttu-id="33861-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33861-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33861-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33861-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33861-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33861-118">INPUTS</span></span>

## <span data-ttu-id="33861-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33861-119">OUTPUTS</span></span>

## <span data-ttu-id="33861-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33861-120">NOTES</span></span>

## <span data-ttu-id="33861-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33861-121">RELATED LINKS</span></span>

[<span data-ttu-id="33861-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33861-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


