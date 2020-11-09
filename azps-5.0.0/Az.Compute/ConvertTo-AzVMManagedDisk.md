---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323395"
---
# <span data-ttu-id="e79b3-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e79b3-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="e79b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e79b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e79b3-103">Blob tabanlı diskler içeren bir sanal makineyi yönetilen diskleri olan bir sanal makineye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="e79b3-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="e79b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e79b3-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e79b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e79b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e79b3-106">**ConvertTo-AzVMManagedDisk** cmdlet 'i, blob tabanlı diskler içeren bir sanal makineyi yönetilen diskleri içeren bir sanal makineye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="e79b3-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="e79b3-107">Bu işlemi çağırmadan önce sanal makinenin durdurulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e79b3-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="e79b3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e79b3-108">EXAMPLES</span></span>

### <span data-ttu-id="e79b3-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e79b3-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="e79b3-110">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' VM01 ' adlı sanal makinenin blob tabanlı disklerini yönetilen disklere dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="e79b3-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="e79b3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e79b3-111">PARAMETERS</span></span>

### <span data-ttu-id="e79b3-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="e79b3-112">-AsJob</span></span>
<span data-ttu-id="e79b3-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e79b3-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79b3-114">-DefaultProfile</span></span>
<span data-ttu-id="e79b3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e79b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e79b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e79b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="e79b3-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e79b3-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e79b3-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="e79b3-118">-VMName</span></span>
<span data-ttu-id="e79b3-119">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e79b3-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="e79b3-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="e79b3-120">-Confirm</span></span>
<span data-ttu-id="e79b3-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e79b3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e79b3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e79b3-122">-WhatIf</span></span>
<span data-ttu-id="e79b3-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e79b3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e79b3-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e79b3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e79b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79b3-125">CommonParameters</span></span>
<span data-ttu-id="e79b3-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e79b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79b3-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e79b3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79b3-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e79b3-128">INPUTS</span></span>

### <span data-ttu-id="e79b3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e79b3-129">System.String</span></span>

## <span data-ttu-id="e79b3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e79b3-130">OUTPUTS</span></span>

### <span data-ttu-id="e79b3-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="e79b3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e79b3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e79b3-132">NOTES</span></span>

## <span data-ttu-id="e79b3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e79b3-133">RELATED LINKS</span></span>
