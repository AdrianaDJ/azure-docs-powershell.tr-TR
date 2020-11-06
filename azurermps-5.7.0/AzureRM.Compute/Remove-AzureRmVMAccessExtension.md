---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589860"
---
# <span data-ttu-id="596c6-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="596c6-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="596c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="596c6-102">SYNOPSIS</span></span>
<span data-ttu-id="596c6-103">Sanal makineden VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="596c6-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="596c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="596c6-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="596c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="596c6-105">DESCRIPTION</span></span>
<span data-ttu-id="596c6-106">**Remove-Azurermvmaccessextenma** cmdlet 'i sanal makine erişimi (VMAccess) sanal makine uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="596c6-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="596c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="596c6-107">EXAMPLES</span></span>

## <span data-ttu-id="596c6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="596c6-108">PARAMETERS</span></span>

### <span data-ttu-id="596c6-109">-Force</span><span class="sxs-lookup"><span data-stu-id="596c6-109">-Force</span></span>
<span data-ttu-id="596c6-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="596c6-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="596c6-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="596c6-111">-Name</span></span>
<span data-ttu-id="596c6-112">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="596c6-112">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596c6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596c6-113">-ResourceGroupName</span></span>
<span data-ttu-id="596c6-114">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="596c6-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596c6-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="596c6-115">-VMName</span></span>
<span data-ttu-id="596c6-116">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="596c6-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="596c6-117">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="596c6-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596c6-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="596c6-118">-Confirm</span></span>
<span data-ttu-id="596c6-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="596c6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596c6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596c6-120">-WhatIf</span></span>
<span data-ttu-id="596c6-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="596c6-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="596c6-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="596c6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596c6-123">CommonParameters</span></span>
<span data-ttu-id="596c6-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="596c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596c6-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596c6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596c6-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="596c6-126">INPUTS</span></span>

### <span data-ttu-id="596c6-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="596c6-127">None</span></span>
<span data-ttu-id="596c6-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="596c6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="596c6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="596c6-129">OUTPUTS</span></span>

## <span data-ttu-id="596c6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="596c6-130">NOTES</span></span>

## <span data-ttu-id="596c6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="596c6-131">RELATED LINKS</span></span>

[<span data-ttu-id="596c6-132">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="596c6-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="596c6-133">Set-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="596c6-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="596c6-134">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="596c6-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
