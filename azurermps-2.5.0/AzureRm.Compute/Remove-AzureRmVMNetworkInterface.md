---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939592"
---
# <span data-ttu-id="d95f7-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d95f7-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="d95f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d95f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d95f7-103">Sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d95f7-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d95f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d95f7-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d95f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d95f7-105">DESCRIPTION</span></span>
<span data-ttu-id="d95f7-106">**Remove-Azurermvmnetworkınterface** cmdlet 'i, bir sanal makineden ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d95f7-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="d95f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d95f7-107">EXAMPLES</span></span>

### <span data-ttu-id="d95f7-108">2</span><span class="sxs-lookup"><span data-stu-id="d95f7-108">1:</span></span>
```

```

## <span data-ttu-id="d95f7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d95f7-109">PARAMETERS</span></span>

### <span data-ttu-id="d95f7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95f7-110">-DefaultProfile</span></span>
<span data-ttu-id="d95f7-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d95f7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95f7-112">-Networkınterfaceds</span><span class="sxs-lookup"><span data-stu-id="d95f7-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="d95f7-113">Bu cmdlet 'in kaldırdığı ağ arabirim kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d95f7-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d95f7-114">-VM</span><span class="sxs-lookup"><span data-stu-id="d95f7-114">-VM</span></span>
<span data-ttu-id="d95f7-115">Bu cmdlet 'in bir ağ arabirimini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d95f7-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="d95f7-116">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d95f7-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="d95f7-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d95f7-117">-Confirm</span></span>
<span data-ttu-id="d95f7-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d95f7-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="d95f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d95f7-119">-WhatIf</span></span>
<span data-ttu-id="d95f7-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d95f7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d95f7-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d95f7-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="d95f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95f7-122">CommonParameters</span></span>
<span data-ttu-id="d95f7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d95f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95f7-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95f7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d95f7-125">INPUTS</span></span>

### <span data-ttu-id="d95f7-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d95f7-126">PSVirtualMachine</span></span>
<span data-ttu-id="d95f7-127">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d95f7-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d95f7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d95f7-128">OUTPUTS</span></span>

### <span data-ttu-id="d95f7-129">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d95f7-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d95f7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d95f7-130">NOTES</span></span>

## <span data-ttu-id="d95f7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d95f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="d95f7-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d95f7-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


