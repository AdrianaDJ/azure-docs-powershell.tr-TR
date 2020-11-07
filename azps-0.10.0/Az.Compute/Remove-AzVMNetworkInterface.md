---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936904"
---
# <span data-ttu-id="99a21-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="99a21-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="99a21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99a21-102">SYNOPSIS</span></span>
<span data-ttu-id="99a21-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99a21-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="99a21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99a21-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99a21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99a21-105">DESCRIPTION</span></span>
<span data-ttu-id="99a21-106">**Remove-Azvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99a21-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="99a21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99a21-107">EXAMPLES</span></span>

### <span data-ttu-id="99a21-108">2</span><span class="sxs-lookup"><span data-stu-id="99a21-108">1:</span></span>
```

```

## <span data-ttu-id="99a21-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99a21-109">PARAMETERS</span></span>

### <span data-ttu-id="99a21-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a21-110">-DefaultProfile</span></span>
<span data-ttu-id="99a21-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99a21-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99a21-112">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="99a21-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="99a21-113">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99a21-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="99a21-114">-VM</span><span class="sxs-lookup"><span data-stu-id="99a21-114">-VM</span></span>
<span data-ttu-id="99a21-115">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="99a21-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="99a21-116">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="99a21-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="99a21-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="99a21-117">-Confirm</span></span>
<span data-ttu-id="99a21-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99a21-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="99a21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a21-119">-WhatIf</span></span>
<span data-ttu-id="99a21-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99a21-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99a21-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99a21-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="99a21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a21-122">CommonParameters</span></span>
<span data-ttu-id="99a21-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99a21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a21-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a21-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a21-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99a21-125">INPUTS</span></span>

### <span data-ttu-id="99a21-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="99a21-126">PSVirtualMachine</span></span>
<span data-ttu-id="99a21-127">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="99a21-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="99a21-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99a21-128">OUTPUTS</span></span>

### <span data-ttu-id="99a21-129">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="99a21-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="99a21-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99a21-130">NOTES</span></span>

## <span data-ttu-id="99a21-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99a21-131">RELATED LINKS</span></span>

[<span data-ttu-id="99a21-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="99a21-132">Get-AzVM</span></span>](./Get-AzVM.md)


