---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef83792704e24102e8e837768ee5acae5abbe548
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572918"
---
# <span data-ttu-id="80131-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="80131-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="80131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80131-102">SYNOPSIS</span></span>
<span data-ttu-id="80131-103">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="80131-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80131-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80131-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80131-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80131-105">DESCRIPTION</span></span>
<span data-ttu-id="80131-106">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="80131-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="80131-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80131-107">EXAMPLES</span></span>

### <span data-ttu-id="80131-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="80131-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="80131-109">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki en son çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="80131-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="80131-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80131-110">PARAMETERS</span></span>

### <span data-ttu-id="80131-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80131-111">-DefaultProfile</span></span>
<span data-ttu-id="80131-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80131-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80131-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80131-113">-ResourceGroupName</span></span>
<span data-ttu-id="80131-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="80131-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="80131-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="80131-115">-VMScaleSetName</span></span>
<span data-ttu-id="80131-116">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="80131-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="80131-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80131-117">CommonParameters</span></span>
<span data-ttu-id="80131-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80131-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80131-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80131-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80131-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80131-120">INPUTS</span></span>

### <span data-ttu-id="80131-121">System. String</span><span class="sxs-lookup"><span data-stu-id="80131-121">System.String</span></span>

## <span data-ttu-id="80131-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80131-122">OUTPUTS</span></span>

### <span data-ttu-id="80131-123">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psrollingupgradestatusınfo</span><span class="sxs-lookup"><span data-stu-id="80131-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="80131-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80131-124">NOTES</span></span>

## <span data-ttu-id="80131-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80131-125">RELATED LINKS</span></span>
