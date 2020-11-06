---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587621"
---
# <span data-ttu-id="87e80-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="87e80-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="87e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e80-102">SYNOPSIS</span></span>
<span data-ttu-id="87e80-103">VMSS için kullanılabilir SKU 'Ları alır.</span><span class="sxs-lookup"><span data-stu-id="87e80-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87e80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87e80-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="87e80-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87e80-105">DESCRIPTION</span></span>
<span data-ttu-id="87e80-106">**Get-AzureRmVmssSku** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="87e80-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="87e80-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87e80-107">EXAMPLES</span></span>

### <span data-ttu-id="87e80-108">Örnek 1: VMSS 'den kullanılabilir tüm STB 'leri alma</span><span class="sxs-lookup"><span data-stu-id="87e80-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="87e80-109">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı tüm mevcut STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="87e80-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="87e80-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87e80-110">PARAMETERS</span></span>

### <span data-ttu-id="87e80-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e80-111">-ResourceGroupName</span></span>
<span data-ttu-id="87e80-112">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87e80-112">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e80-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="87e80-113">-VMScaleSetName</span></span>
<span data-ttu-id="87e80-114">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="87e80-114">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e80-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e80-115">CommonParameters</span></span>
<span data-ttu-id="87e80-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87e80-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e80-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e80-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e80-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87e80-118">INPUTS</span></span>

### <span data-ttu-id="87e80-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="87e80-119">None</span></span>
<span data-ttu-id="87e80-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="87e80-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87e80-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87e80-121">OUTPUTS</span></span>

### <span data-ttu-id="87e80-122">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="87e80-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="87e80-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87e80-123">NOTES</span></span>

## <span data-ttu-id="87e80-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87e80-124">RELATED LINKS</span></span>

[<span data-ttu-id="87e80-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="87e80-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


