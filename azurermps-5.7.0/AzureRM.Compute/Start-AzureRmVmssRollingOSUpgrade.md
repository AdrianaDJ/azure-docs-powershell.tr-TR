---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: e02bc88b8f8a3436270f48aea6d9d316dab79318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764466"
---
# <span data-ttu-id="495ce-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="495ce-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="495ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495ce-102">SYNOPSIS</span></span>
<span data-ttu-id="495ce-103">Tüm sanal makine ölçek kümesi örneklerini kullanılabilir en son Platform görüntüsü işletim sistemi sürümüne taşımak için çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="495ce-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="495ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="495ce-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="495ce-105">DESCRIPTION</span></span>
<span data-ttu-id="495ce-106">Tüm sanal makine ölçek kümesi örneklerini kullanılabilir en son Platform görüntüsü işletim sistemi sürümüne taşımak için çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="495ce-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="495ce-107">En son işletim sistemi sürümünü çalıştıran örnekler etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="495ce-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="495ce-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="495ce-108">EXAMPLES</span></span>

### <span data-ttu-id="495ce-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="495ce-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="495ce-110">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi 'nin tüm VM örneklerinin çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="495ce-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="495ce-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="495ce-111">PARAMETERS</span></span>

### <span data-ttu-id="495ce-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="495ce-112">-AsJob</span></span>
<span data-ttu-id="495ce-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="495ce-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495ce-114">-DefaultProfile</span></span>
<span data-ttu-id="495ce-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="495ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="495ce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495ce-116">-ResourceGroupName</span></span>
<span data-ttu-id="495ce-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="495ce-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="495ce-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="495ce-118">-VMScaleSetName</span></span>
<span data-ttu-id="495ce-119">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="495ce-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="495ce-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="495ce-120">-Confirm</span></span>
<span data-ttu-id="495ce-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="495ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495ce-122">-WhatIf</span></span>
<span data-ttu-id="495ce-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="495ce-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495ce-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="495ce-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495ce-125">CommonParameters</span></span>
<span data-ttu-id="495ce-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="495ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495ce-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495ce-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495ce-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="495ce-128">INPUTS</span></span>

### <span data-ttu-id="495ce-129">System. String</span><span class="sxs-lookup"><span data-stu-id="495ce-129">System.String</span></span>

## <span data-ttu-id="495ce-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="495ce-130">OUTPUTS</span></span>

### <span data-ttu-id="495ce-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="495ce-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="495ce-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="495ce-132">NOTES</span></span>

## <span data-ttu-id="495ce-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="495ce-133">RELATED LINKS</span></span>
