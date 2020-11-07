---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939752"
---
# <span data-ttu-id="07a0d-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="07a0d-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="07a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="07a0d-103">Sanal makineden VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07a0d-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07a0d-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="07a0d-106">**Remove-Azurermvmaccessextenma** cmdlet 'i sanal makine erişimi (VMAccess) sanal makine uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07a0d-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="07a0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07a0d-107">EXAMPLES</span></span>

## <span data-ttu-id="07a0d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07a0d-108">PARAMETERS</span></span>

### <span data-ttu-id="07a0d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a0d-109">-DefaultProfile</span></span>
<span data-ttu-id="07a0d-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07a0d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07a0d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="07a0d-111">-Force</span></span>
<span data-ttu-id="07a0d-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="07a0d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07a0d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="07a0d-113">-Name</span></span>
<span data-ttu-id="07a0d-114">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07a0d-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="07a0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="07a0d-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07a0d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="07a0d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="07a0d-117">-VMName</span></span>
<span data-ttu-id="07a0d-118">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07a0d-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="07a0d-119">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07a0d-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="07a0d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="07a0d-120">-Confirm</span></span>
<span data-ttu-id="07a0d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07a0d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a0d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a0d-122">-WhatIf</span></span>
<span data-ttu-id="07a0d-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07a0d-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="07a0d-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07a0d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a0d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a0d-125">CommonParameters</span></span>
<span data-ttu-id="07a0d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07a0d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a0d-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a0d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a0d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07a0d-128">INPUTS</span></span>

### <span data-ttu-id="07a0d-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07a0d-129">None</span></span>
<span data-ttu-id="07a0d-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="07a0d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07a0d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07a0d-131">OUTPUTS</span></span>

### <span data-ttu-id="07a0d-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="07a0d-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="07a0d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07a0d-133">NOTES</span></span>

## <span data-ttu-id="07a0d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07a0d-134">RELATED LINKS</span></span>

[<span data-ttu-id="07a0d-135">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="07a0d-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="07a0d-136">Set-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="07a0d-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="07a0d-137">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="07a0d-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
