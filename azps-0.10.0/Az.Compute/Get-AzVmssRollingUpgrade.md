---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3e89a549b665ff686cc773fa18cf0fceb22014ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936997"
---
# <span data-ttu-id="f6a02-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f6a02-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="f6a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6a02-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a02-103">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6a02-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f6a02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6a02-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6a02-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a02-106">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6a02-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f6a02-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6a02-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a02-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f6a02-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f6a02-109">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki en son çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6a02-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f6a02-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6a02-110">PARAMETERS</span></span>

### <span data-ttu-id="f6a02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a02-111">-DefaultProfile</span></span>
<span data-ttu-id="f6a02-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6a02-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a02-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a02-113">-ResourceGroupName</span></span>
<span data-ttu-id="f6a02-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f6a02-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6a02-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f6a02-115">-VMScaleSetName</span></span>
<span data-ttu-id="f6a02-116">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="f6a02-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="f6a02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a02-117">CommonParameters</span></span>
<span data-ttu-id="f6a02-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6a02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a02-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a02-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a02-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6a02-120">INPUTS</span></span>

### <span data-ttu-id="f6a02-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f6a02-121">System.String</span></span>

## <span data-ttu-id="f6a02-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6a02-122">OUTPUTS</span></span>

### <span data-ttu-id="f6a02-123">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psrollingupgradestatusınfo</span><span class="sxs-lookup"><span data-stu-id="f6a02-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="f6a02-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6a02-124">NOTES</span></span>

## <span data-ttu-id="f6a02-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6a02-125">RELATED LINKS</span></span>

