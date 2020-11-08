---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276414"
---
# <span data-ttu-id="5c03e-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="5c03e-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="5c03e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c03e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c03e-103">VMSS için kullanılabilir SKU 'Ları alır.</span><span class="sxs-lookup"><span data-stu-id="5c03e-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="5c03e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c03e-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c03e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c03e-105">DESCRIPTION</span></span>
<span data-ttu-id="5c03e-106">**Get-AzVmssSku** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="5c03e-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5c03e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c03e-107">EXAMPLES</span></span>

### <span data-ttu-id="5c03e-108">Örnek 1: VMSS 'den kullanılabilir tüm STB 'leri alma</span><span class="sxs-lookup"><span data-stu-id="5c03e-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="5c03e-109">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı tüm mevcut STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="5c03e-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="5c03e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c03e-110">PARAMETERS</span></span>

### <span data-ttu-id="5c03e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c03e-111">-DefaultProfile</span></span>
<span data-ttu-id="5c03e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c03e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c03e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c03e-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c03e-114">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c03e-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="5c03e-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5c03e-115">-VMScaleSetName</span></span>
<span data-ttu-id="5c03e-116">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="5c03e-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c03e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c03e-117">CommonParameters</span></span>
<span data-ttu-id="5c03e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c03e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c03e-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c03e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c03e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c03e-120">INPUTS</span></span>

### <span data-ttu-id="5c03e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5c03e-121">System.String</span></span>

## <span data-ttu-id="5c03e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c03e-122">OUTPUTS</span></span>

### <span data-ttu-id="5c03e-123">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="5c03e-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="5c03e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c03e-124">NOTES</span></span>

## <span data-ttu-id="5c03e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c03e-125">RELATED LINKS</span></span>

[<span data-ttu-id="5c03e-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c03e-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


