---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: ce16c011d07d47dcbbfd0a957323955904751c82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917292"
---
# <span data-ttu-id="03241-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="03241-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="03241-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03241-102">SYNOPSIS</span></span>
<span data-ttu-id="03241-103">Sanal makineden uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="03241-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="03241-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03241-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03241-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03241-105">DESCRIPTION</span></span>
<span data-ttu-id="03241-106">**Remove-Azvmexter** cmdlet 'i, sanal makinenin sanal makine uzantılarından bir uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="03241-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="03241-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03241-107">EXAMPLES</span></span>

### <span data-ttu-id="03241-108">Örnek 1: sanal makineden uzantıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="03241-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="03241-109">Bu komut, ResourceGroup11 'da VirtualMachine22 adındaki sanal makineden ContosoTest adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="03241-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="03241-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03241-110">PARAMETERS</span></span>

### <span data-ttu-id="03241-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03241-111">-DefaultProfile</span></span>
<span data-ttu-id="03241-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03241-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03241-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03241-113">-Force</span></span>
<span data-ttu-id="03241-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="03241-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03241-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="03241-115">-Name</span></span>
<span data-ttu-id="03241-116">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03241-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03241-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03241-117">-ResourceGroupName</span></span>
<span data-ttu-id="03241-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03241-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03241-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="03241-119">-VMName</span></span>
<span data-ttu-id="03241-120">Bu cmdlet 'in uzantıyı kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03241-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03241-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="03241-121">-Confirm</span></span>
<span data-ttu-id="03241-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03241-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03241-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03241-123">-WhatIf</span></span>
<span data-ttu-id="03241-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03241-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03241-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03241-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03241-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03241-126">CommonParameters</span></span>
<span data-ttu-id="03241-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03241-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03241-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03241-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03241-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03241-129">INPUTS</span></span>

### <span data-ttu-id="03241-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03241-130">System.String</span></span>

## <span data-ttu-id="03241-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03241-131">OUTPUTS</span></span>

### <span data-ttu-id="03241-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="03241-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="03241-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03241-133">NOTES</span></span>

## <span data-ttu-id="03241-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03241-134">RELATED LINKS</span></span>

[<span data-ttu-id="03241-135">Get-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="03241-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="03241-136">Set-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="03241-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


