---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: b77d741c0313e202304be3fd51fb3e1cd5b25b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586963"
---
# <span data-ttu-id="dd9a9-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd9a9-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="dd9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9a9-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd9a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd9a9-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd9a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="dd9a9-106">**Remove-Azurermvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="dd9a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd9a9-107">EXAMPLES</span></span>

## <span data-ttu-id="dd9a9-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd9a9-108">PARAMETERS</span></span>

### <span data-ttu-id="dd9a9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9a9-109">-DefaultProfile</span></span>
<span data-ttu-id="dd9a9-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd9a9-111">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="dd9a9-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="dd9a9-112">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd9a9-113">-VM</span><span class="sxs-lookup"><span data-stu-id="dd9a9-113">-VM</span></span>
<span data-ttu-id="dd9a9-114">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="dd9a9-115">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="dd9a9-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd9a9-116">-Confirm</span></span>
<span data-ttu-id="dd9a9-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-117">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="dd9a9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd9a9-118">-WhatIf</span></span>
<span data-ttu-id="dd9a9-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd9a9-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-120">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="dd9a9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9a9-121">CommonParameters</span></span>
<span data-ttu-id="dd9a9-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9a9-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd9a9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9a9-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd9a9-124">INPUTS</span></span>

## <span data-ttu-id="dd9a9-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd9a9-125">OUTPUTS</span></span>

## <span data-ttu-id="dd9a9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd9a9-126">NOTES</span></span>

## <span data-ttu-id="dd9a9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd9a9-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd9a9-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dd9a9-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


