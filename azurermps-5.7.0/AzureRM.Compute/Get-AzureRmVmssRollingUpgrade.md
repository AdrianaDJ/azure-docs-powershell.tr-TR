---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef9d1ac2e5bca51ee1addf8fdffd87c5045d23eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764474"
---
# <span data-ttu-id="0de0d-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="0de0d-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="0de0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0de0d-103">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0de0d-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0de0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0de0d-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0de0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0de0d-105">DESCRIPTION</span></span>
<span data-ttu-id="0de0d-106">En son sanal makine ölçek kümesi çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0de0d-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="0de0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0de0d-107">EXAMPLES</span></span>

### <span data-ttu-id="0de0d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0de0d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0de0d-109">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki en son çalışırken yükseltmenin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0de0d-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0de0d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0de0d-110">PARAMETERS</span></span>

### <span data-ttu-id="0de0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de0d-111">-DefaultProfile</span></span>
<span data-ttu-id="0de0d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0de0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0de0d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de0d-113">-ResourceGroupName</span></span>
<span data-ttu-id="0de0d-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0de0d-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0de0d-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0de0d-115">-VMScaleSetName</span></span>
<span data-ttu-id="0de0d-116">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="0de0d-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="0de0d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de0d-117">CommonParameters</span></span>
<span data-ttu-id="0de0d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0de0d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de0d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de0d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de0d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0de0d-120">INPUTS</span></span>

### <span data-ttu-id="0de0d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0de0d-121">System.String</span></span>

## <span data-ttu-id="0de0d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0de0d-122">OUTPUTS</span></span>

### <span data-ttu-id="0de0d-123">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psrollingupgradestatusınfo</span><span class="sxs-lookup"><span data-stu-id="0de0d-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="0de0d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0de0d-124">NOTES</span></span>

## <span data-ttu-id="0de0d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0de0d-125">RELATED LINKS</span></span>
