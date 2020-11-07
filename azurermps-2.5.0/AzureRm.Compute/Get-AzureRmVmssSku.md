---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939609"
---
# <span data-ttu-id="edb0f-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="edb0f-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="edb0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb0f-102">SYNOPSIS</span></span>
<span data-ttu-id="edb0f-103">VMSS için kullanılabilir SKU 'Ları alır.</span><span class="sxs-lookup"><span data-stu-id="edb0f-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edb0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edb0f-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edb0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edb0f-105">DESCRIPTION</span></span>
<span data-ttu-id="edb0f-106">**Get-AzureRmVmssSku** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="edb0f-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="edb0f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edb0f-107">EXAMPLES</span></span>

### <span data-ttu-id="edb0f-108">Örnek 1: VMSS 'den kullanılabilir tüm STB 'leri alma</span><span class="sxs-lookup"><span data-stu-id="edb0f-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="edb0f-109">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı tüm mevcut STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="edb0f-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="edb0f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edb0f-110">PARAMETERS</span></span>

### <span data-ttu-id="edb0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb0f-111">-DefaultProfile</span></span>
<span data-ttu-id="edb0f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edb0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb0f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb0f-113">-ResourceGroupName</span></span>
<span data-ttu-id="edb0f-114">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edb0f-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="edb0f-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="edb0f-115">-VMScaleSetName</span></span>
<span data-ttu-id="edb0f-116">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="edb0f-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="edb0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb0f-117">CommonParameters</span></span>
<span data-ttu-id="edb0f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edb0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb0f-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb0f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb0f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edb0f-120">INPUTS</span></span>

### <span data-ttu-id="edb0f-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="edb0f-121">None</span></span>
<span data-ttu-id="edb0f-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="edb0f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="edb0f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edb0f-123">OUTPUTS</span></span>

### <span data-ttu-id="edb0f-124">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="edb0f-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="edb0f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edb0f-125">NOTES</span></span>

## <span data-ttu-id="edb0f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edb0f-126">RELATED LINKS</span></span>

[<span data-ttu-id="edb0f-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="edb0f-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


