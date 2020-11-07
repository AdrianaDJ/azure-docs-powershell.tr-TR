---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: d005f3f182109399f5a74b934959951dfb02c48e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936998"
---
# <span data-ttu-id="bc1ec-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="bc1ec-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="bc1ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1ec-103">VMSS için kullanılabilir SKU 'Ları alır.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="bc1ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc1ec-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc1ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="bc1ec-106">**Get-AzVmssSku** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bc1ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="bc1ec-108">Örnek 1: VMSS 'den kullanılabilir tüm STB 'leri alma</span><span class="sxs-lookup"><span data-stu-id="bc1ec-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="bc1ec-109">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı tüm mevcut STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="bc1ec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc1ec-110">PARAMETERS</span></span>

### <span data-ttu-id="bc1ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1ec-111">-DefaultProfile</span></span>
<span data-ttu-id="bc1ec-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc1ec-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc1ec-113">-ResourceGroupName</span></span>
<span data-ttu-id="bc1ec-114">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bc1ec-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bc1ec-115">-VMScaleSetName</span></span>
<span data-ttu-id="bc1ec-116">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="bc1ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1ec-117">CommonParameters</span></span>
<span data-ttu-id="bc1ec-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1ec-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc1ec-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1ec-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc1ec-120">INPUTS</span></span>

### <span data-ttu-id="bc1ec-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc1ec-121">None</span></span>
<span data-ttu-id="bc1ec-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc1ec-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc1ec-123">OUTPUTS</span></span>

### <span data-ttu-id="bc1ec-124">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bc1ec-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="bc1ec-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc1ec-125">NOTES</span></span>

## <span data-ttu-id="bc1ec-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc1ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="bc1ec-127">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="bc1ec-127">Get-AzVmss</span></span>](./Get-AzVmss.md)


