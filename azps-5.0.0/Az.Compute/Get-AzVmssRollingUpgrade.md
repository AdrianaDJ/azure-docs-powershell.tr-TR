---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323359"
---
# <span data-ttu-id="dafdc-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="dafdc-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="dafdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dafdc-102">SYNOPSIS</span></span>
<span data-ttu-id="dafdc-103">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="dafdc-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="dafdc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dafdc-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafdc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dafdc-105">DESCRIPTION</span></span>
<span data-ttu-id="dafdc-106">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="dafdc-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="dafdc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dafdc-107">EXAMPLES</span></span>

### <span data-ttu-id="dafdc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dafdc-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="dafdc-109">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki en son çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="dafdc-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="dafdc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dafdc-110">PARAMETERS</span></span>

### <span data-ttu-id="dafdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafdc-111">-DefaultProfile</span></span>
<span data-ttu-id="dafdc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dafdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dafdc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dafdc-113">-ResourceGroupName</span></span>
<span data-ttu-id="dafdc-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dafdc-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="dafdc-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dafdc-115">-VMScaleSetName</span></span>
<span data-ttu-id="dafdc-116">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="dafdc-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="dafdc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafdc-117">CommonParameters</span></span>
<span data-ttu-id="dafdc-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dafdc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafdc-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dafdc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafdc-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dafdc-120">INPUTS</span></span>

### <span data-ttu-id="dafdc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dafdc-121">System.String</span></span>

## <span data-ttu-id="dafdc-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dafdc-122">OUTPUTS</span></span>

### <span data-ttu-id="dafdc-123">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psrollingupgradestatusınfo</span><span class="sxs-lookup"><span data-stu-id="dafdc-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="dafdc-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dafdc-124">NOTES</span></span>

## <span data-ttu-id="dafdc-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dafdc-125">RELATED LINKS</span></span>
