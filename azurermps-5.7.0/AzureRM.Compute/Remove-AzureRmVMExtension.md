---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586794"
---
# <span data-ttu-id="63ddb-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="63ddb-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="63ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="63ddb-103">Sanal makineden uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63ddb-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63ddb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63ddb-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63ddb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="63ddb-106">**Remove-Azurermvmexter** cmdlet 'i, sanal makinenin sanal makine uzantılarından bir uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63ddb-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="63ddb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63ddb-107">EXAMPLES</span></span>

### <span data-ttu-id="63ddb-108">Örnek 1: sanal makineden uzantıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="63ddb-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="63ddb-109">Bu komut, ResourceGroup11 'da VirtualMachine22 adındaki sanal makineden ContosoTest adlı uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63ddb-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="63ddb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63ddb-110">PARAMETERS</span></span>

### <span data-ttu-id="63ddb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="63ddb-111">-Force</span></span>
<span data-ttu-id="63ddb-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="63ddb-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63ddb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="63ddb-113">-Name</span></span>
<span data-ttu-id="63ddb-114">Bu cmdlet 'in kaldırdığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63ddb-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63ddb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ddb-115">-ResourceGroupName</span></span>
<span data-ttu-id="63ddb-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63ddb-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="63ddb-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="63ddb-117">-VMName</span></span>
<span data-ttu-id="63ddb-118">Bu cmdlet 'in uzantıyı kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63ddb-118">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="63ddb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="63ddb-119">-Confirm</span></span>
<span data-ttu-id="63ddb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63ddb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ddb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ddb-121">-WhatIf</span></span>
<span data-ttu-id="63ddb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63ddb-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="63ddb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63ddb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ddb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ddb-124">CommonParameters</span></span>
<span data-ttu-id="63ddb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63ddb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ddb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ddb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ddb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63ddb-127">INPUTS</span></span>

### <span data-ttu-id="63ddb-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="63ddb-128">None</span></span>
<span data-ttu-id="63ddb-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="63ddb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63ddb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63ddb-130">OUTPUTS</span></span>

## <span data-ttu-id="63ddb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63ddb-131">NOTES</span></span>

## <span data-ttu-id="63ddb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63ddb-132">RELATED LINKS</span></span>

[<span data-ttu-id="63ddb-133">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="63ddb-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="63ddb-134">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="63ddb-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


