---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: d5aba3e8810ef06e81b62803cb6b71dd8de619ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761277"
---
# <span data-ttu-id="28c3a-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="28c3a-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="28c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="28c3a-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28c3a-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="28c3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28c3a-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="28c3a-106">**Remove-Azvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28c3a-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="28c3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28c3a-107">EXAMPLES</span></span>

## <span data-ttu-id="28c3a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28c3a-108">PARAMETERS</span></span>

### <span data-ttu-id="28c3a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c3a-109">-DefaultProfile</span></span>
<span data-ttu-id="28c3a-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28c3a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28c3a-111">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="28c3a-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="28c3a-112">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28c3a-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="28c3a-113">-VM</span><span class="sxs-lookup"><span data-stu-id="28c3a-113">-VM</span></span>
<span data-ttu-id="28c3a-114">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="28c3a-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="28c3a-115">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="28c3a-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="28c3a-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="28c3a-116">-Confirm</span></span>
<span data-ttu-id="28c3a-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28c3a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c3a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c3a-118">-WhatIf</span></span>
<span data-ttu-id="28c3a-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28c3a-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28c3a-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28c3a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c3a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c3a-121">CommonParameters</span></span>
<span data-ttu-id="28c3a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28c3a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c3a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c3a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c3a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28c3a-124">INPUTS</span></span>

### <span data-ttu-id="28c3a-125">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="28c3a-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="28c3a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28c3a-126">OUTPUTS</span></span>

### <span data-ttu-id="28c3a-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="28c3a-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="28c3a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28c3a-128">NOTES</span></span>

## <span data-ttu-id="28c3a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28c3a-129">RELATED LINKS</span></span>

[<span data-ttu-id="28c3a-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="28c3a-130">Get-AzVM</span></span>](./Get-AzVM.md)


