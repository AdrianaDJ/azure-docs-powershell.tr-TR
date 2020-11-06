---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586793"
---
# <span data-ttu-id="cd0b7-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd0b7-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="cd0b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0b7-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd0b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd0b7-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="cd0b7-106">**Remove-Azurermvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="cd0b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd0b7-107">EXAMPLES</span></span>

## <span data-ttu-id="cd0b7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd0b7-108">PARAMETERS</span></span>

### <span data-ttu-id="cd0b7-109">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="cd0b7-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="cd0b7-110">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0b7-111">-VM</span><span class="sxs-lookup"><span data-stu-id="cd0b7-111">-VM</span></span>
<span data-ttu-id="cd0b7-112">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="cd0b7-113">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0b7-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd0b7-114">-Confirm</span></span>
<span data-ttu-id="cd0b7-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-115">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0b7-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0b7-116">-WhatIf</span></span>
<span data-ttu-id="cd0b7-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd0b7-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-118">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0b7-119">CommonParameters</span></span>
<span data-ttu-id="cd0b7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0b7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0b7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0b7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd0b7-122">INPUTS</span></span>

### <span data-ttu-id="cd0b7-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cd0b7-123">None</span></span>
<span data-ttu-id="cd0b7-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cd0b7-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd0b7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd0b7-125">OUTPUTS</span></span>

## <span data-ttu-id="cd0b7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd0b7-126">NOTES</span></span>

## <span data-ttu-id="cd0b7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd0b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="cd0b7-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd0b7-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


