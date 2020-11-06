---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c906d7b0b10197e934ace7f9c913ee36e02be7ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593305"
---
# <span data-ttu-id="82b09-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="82b09-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="82b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82b09-102">SYNOPSIS</span></span>
<span data-ttu-id="82b09-103">VMSS için kullanılabilir SKU 'Ları alır.</span><span class="sxs-lookup"><span data-stu-id="82b09-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82b09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82b09-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82b09-105">DESCRIPTION</span></span>
<span data-ttu-id="82b09-106">**Get-AzureRmVmssSku** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="82b09-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="82b09-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82b09-107">EXAMPLES</span></span>

### <span data-ttu-id="82b09-108">Örnek 1: VMSS 'den kullanılabilir tüm STB 'leri alma</span><span class="sxs-lookup"><span data-stu-id="82b09-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="82b09-109">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı tüm mevcut STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="82b09-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="82b09-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82b09-110">PARAMETERS</span></span>

### <span data-ttu-id="82b09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b09-111">-DefaultProfile</span></span>
<span data-ttu-id="82b09-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82b09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82b09-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b09-113">-ResourceGroupName</span></span>
<span data-ttu-id="82b09-114">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82b09-114">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b09-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="82b09-115">-VMScaleSetName</span></span>
<span data-ttu-id="82b09-116">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="82b09-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b09-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b09-117">CommonParameters</span></span>
<span data-ttu-id="82b09-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82b09-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b09-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b09-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b09-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82b09-120">INPUTS</span></span>

### <span data-ttu-id="82b09-121">System. String</span><span class="sxs-lookup"><span data-stu-id="82b09-121">System.String</span></span>

## <span data-ttu-id="82b09-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82b09-122">OUTPUTS</span></span>

### <span data-ttu-id="82b09-123">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="82b09-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="82b09-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82b09-124">NOTES</span></span>

## <span data-ttu-id="82b09-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82b09-125">RELATED LINKS</span></span>

[<span data-ttu-id="82b09-126">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82b09-126">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


