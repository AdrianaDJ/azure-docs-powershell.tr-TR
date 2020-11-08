---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267895"
---
# <span data-ttu-id="c32f0-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c32f0-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="c32f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c32f0-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c32f0-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c32f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c32f0-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c32f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c32f0-105">DESCRIPTION</span></span>
<span data-ttu-id="c32f0-106">**Remove-Azvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c32f0-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c32f0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c32f0-107">EXAMPLES</span></span>

## <span data-ttu-id="c32f0-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c32f0-108">PARAMETERS</span></span>

### <span data-ttu-id="c32f0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32f0-109">-DefaultProfile</span></span>
<span data-ttu-id="c32f0-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c32f0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c32f0-111">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="c32f0-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="c32f0-112">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32f0-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32f0-113">-VM</span><span class="sxs-lookup"><span data-stu-id="c32f0-113">-VM</span></span>
<span data-ttu-id="c32f0-114">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c32f0-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="c32f0-115">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c32f0-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c32f0-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="c32f0-116">-Confirm</span></span>
<span data-ttu-id="c32f0-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c32f0-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32f0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c32f0-118">-WhatIf</span></span>
<span data-ttu-id="c32f0-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c32f0-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c32f0-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c32f0-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32f0-121">CommonParameters</span></span>
<span data-ttu-id="c32f0-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c32f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32f0-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c32f0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32f0-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c32f0-124">INPUTS</span></span>

### <span data-ttu-id="c32f0-125">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c32f0-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c32f0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c32f0-126">OUTPUTS</span></span>

### <span data-ttu-id="c32f0-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c32f0-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c32f0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c32f0-128">NOTES</span></span>

## <span data-ttu-id="c32f0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c32f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="c32f0-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c32f0-130">Get-AzVM</span></span>](./Get-AzVM.md)


