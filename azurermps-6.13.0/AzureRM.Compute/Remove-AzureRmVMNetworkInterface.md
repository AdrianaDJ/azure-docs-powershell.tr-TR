---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763896"
---
# <span data-ttu-id="40b83-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="40b83-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="40b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b83-102">SYNOPSIS</span></span>
<span data-ttu-id="40b83-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="40b83-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40b83-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40b83-105">DESCRIPTION</span></span>
<span data-ttu-id="40b83-106">**Remove-Azurermvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="40b83-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="40b83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40b83-107">EXAMPLES</span></span>

## <span data-ttu-id="40b83-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40b83-108">PARAMETERS</span></span>

### <span data-ttu-id="40b83-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b83-109">-DefaultProfile</span></span>
<span data-ttu-id="40b83-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40b83-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b83-111">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="40b83-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="40b83-112">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40b83-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="40b83-113">-VM</span><span class="sxs-lookup"><span data-stu-id="40b83-113">-VM</span></span>
<span data-ttu-id="40b83-114">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="40b83-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="40b83-115">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="40b83-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="40b83-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="40b83-116">-Confirm</span></span>
<span data-ttu-id="40b83-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40b83-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b83-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b83-118">-WhatIf</span></span>
<span data-ttu-id="40b83-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40b83-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40b83-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40b83-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b83-121">CommonParameters</span></span>
<span data-ttu-id="40b83-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40b83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b83-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b83-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40b83-124">INPUTS</span></span>

### <span data-ttu-id="40b83-125">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="40b83-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="40b83-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40b83-126">OUTPUTS</span></span>

### <span data-ttu-id="40b83-127">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="40b83-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="40b83-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40b83-128">NOTES</span></span>

## <span data-ttu-id="40b83-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40b83-129">RELATED LINKS</span></span>

[<span data-ttu-id="40b83-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="40b83-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

