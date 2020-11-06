---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 7f4e28c00b0238b519ad2b038676a295147b5c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592242"
---
# <span data-ttu-id="90304-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="90304-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="90304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90304-102">SYNOPSIS</span></span>
<span data-ttu-id="90304-103">Tüm sanal makine ölçek kümesi örneklerini kullanılabilir en son Platform görüntüsü işletim sistemi sürümüne taşımak için çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="90304-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90304-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90304-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90304-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90304-105">DESCRIPTION</span></span>
<span data-ttu-id="90304-106">Tüm sanal makine ölçek kümesi örneklerini kullanılabilir en son Platform görüntüsü işletim sistemi sürümüne taşımak için çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="90304-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="90304-107">En son işletim sistemi sürümünü çalıştıran örnekler etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="90304-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="90304-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90304-108">EXAMPLES</span></span>

### <span data-ttu-id="90304-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90304-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="90304-110">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi 'nin tüm VM örneklerinin çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="90304-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="90304-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90304-111">PARAMETERS</span></span>

### <span data-ttu-id="90304-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90304-112">-DefaultProfile</span></span>
<span data-ttu-id="90304-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90304-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90304-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90304-114">-ResourceGroupName</span></span>
<span data-ttu-id="90304-115">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="90304-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="90304-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="90304-116">-VMScaleSetName</span></span>
<span data-ttu-id="90304-117">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="90304-117">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="90304-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="90304-118">-Confirm</span></span>
<span data-ttu-id="90304-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90304-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90304-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90304-120">-WhatIf</span></span>
<span data-ttu-id="90304-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90304-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90304-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90304-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90304-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90304-123">CommonParameters</span></span>
<span data-ttu-id="90304-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90304-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90304-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90304-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90304-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90304-126">INPUTS</span></span>

### <span data-ttu-id="90304-127">System. String</span><span class="sxs-lookup"><span data-stu-id="90304-127">System.String</span></span>

## <span data-ttu-id="90304-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90304-128">OUTPUTS</span></span>

### <span data-ttu-id="90304-129">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="90304-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="90304-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90304-130">NOTES</span></span>

## <span data-ttu-id="90304-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90304-131">RELATED LINKS</span></span>

