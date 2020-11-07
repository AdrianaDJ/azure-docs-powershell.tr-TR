---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936923"
---
# <span data-ttu-id="62ecf-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="62ecf-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="62ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="62ecf-103">Sanal makineden VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62ecf-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="62ecf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62ecf-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ecf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="62ecf-106">**Remove-Azvmaccessextenma** cmdlet 'i sanal makine erişimi (VMAccess) sanal makine uzantısını bir sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62ecf-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="62ecf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62ecf-107">EXAMPLES</span></span>

## <span data-ttu-id="62ecf-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62ecf-108">PARAMETERS</span></span>

### <span data-ttu-id="62ecf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ecf-109">-DefaultProfile</span></span>
<span data-ttu-id="62ecf-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62ecf-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ecf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="62ecf-111">-Force</span></span>
<span data-ttu-id="62ecf-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="62ecf-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62ecf-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="62ecf-113">-Name</span></span>
<span data-ttu-id="62ecf-114">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62ecf-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62ecf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ecf-115">-ResourceGroupName</span></span>
<span data-ttu-id="62ecf-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62ecf-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="62ecf-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="62ecf-117">-VMName</span></span>
<span data-ttu-id="62ecf-118">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62ecf-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="62ecf-119">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62ecf-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="62ecf-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="62ecf-120">-Confirm</span></span>
<span data-ttu-id="62ecf-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62ecf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ecf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ecf-122">-WhatIf</span></span>
<span data-ttu-id="62ecf-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62ecf-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="62ecf-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62ecf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ecf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ecf-125">CommonParameters</span></span>
<span data-ttu-id="62ecf-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62ecf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ecf-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ecf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ecf-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62ecf-128">INPUTS</span></span>

### <span data-ttu-id="62ecf-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62ecf-129">None</span></span>
<span data-ttu-id="62ecf-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="62ecf-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62ecf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62ecf-131">OUTPUTS</span></span>

### <span data-ttu-id="62ecf-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="62ecf-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="62ecf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62ecf-133">NOTES</span></span>

## <span data-ttu-id="62ecf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62ecf-134">RELATED LINKS</span></span>

[<span data-ttu-id="62ecf-135">Get-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="62ecf-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="62ecf-136">Set-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="62ecf-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="62ecf-137">Remove-Azvmexgergeri</span><span class="sxs-lookup"><span data-stu-id="62ecf-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
