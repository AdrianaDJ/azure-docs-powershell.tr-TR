---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: 835413728b22dd8bbb80d472eed71e0f4185db89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939593"
---
# <span data-ttu-id="18f5d-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="18f5d-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="18f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="18f5d-103">Sanal makineden uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18f5d-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18f5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18f5d-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18f5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="18f5d-106">**Remove-Azurermvmexter** cmdlet 'i, sanal makinenin sanal makine uzantılarından bir uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18f5d-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="18f5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18f5d-107">EXAMPLES</span></span>

### <span data-ttu-id="18f5d-108">Örnek 1: sanal makineden uzantıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="18f5d-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="18f5d-109">Bu komut, ResourceGroup11 'da VirtualMachine22 adındaki sanal makineden ContosoTest adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18f5d-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="18f5d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18f5d-110">PARAMETERS</span></span>

### <span data-ttu-id="18f5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f5d-111">-DefaultProfile</span></span>
<span data-ttu-id="18f5d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18f5d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18f5d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="18f5d-113">-Force</span></span>
<span data-ttu-id="18f5d-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="18f5d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18f5d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="18f5d-115">-Name</span></span>
<span data-ttu-id="18f5d-116">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f5d-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18f5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18f5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="18f5d-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f5d-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="18f5d-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="18f5d-119">-VMName</span></span>
<span data-ttu-id="18f5d-120">Bu cmdlet 'in uzantıyı kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f5d-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="18f5d-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="18f5d-121">-Confirm</span></span>
<span data-ttu-id="18f5d-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18f5d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18f5d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18f5d-123">-WhatIf</span></span>
<span data-ttu-id="18f5d-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18f5d-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="18f5d-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18f5d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18f5d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f5d-126">CommonParameters</span></span>
<span data-ttu-id="18f5d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18f5d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f5d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f5d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f5d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18f5d-129">INPUTS</span></span>

### <span data-ttu-id="18f5d-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="18f5d-130">None</span></span>
<span data-ttu-id="18f5d-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="18f5d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18f5d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18f5d-132">OUTPUTS</span></span>

### <span data-ttu-id="18f5d-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="18f5d-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="18f5d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18f5d-134">NOTES</span></span>

## <span data-ttu-id="18f5d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18f5d-135">RELATED LINKS</span></span>

[<span data-ttu-id="18f5d-136">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="18f5d-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="18f5d-137">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="18f5d-137">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


