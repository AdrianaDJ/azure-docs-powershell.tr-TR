---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 14f29bb7097f584c89fa1bf92bf816cf4ca3d511
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104652"
---
# <span data-ttu-id="62f6d-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="62f6d-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="62f6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="62f6d-103">VM ölçeklendirme kümesinde disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="62f6d-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="62f6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62f6d-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62f6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="62f6d-106">VM ölçeklendirme kümesinde disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="62f6d-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="62f6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62f6d-107">EXAMPLES</span></span>

### <span data-ttu-id="62f6d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62f6d-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="62f6d-109">Group001 adındaki kaynak grubuna ait olan VMSS001 adlı VM Ölçek kümesindeki disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="62f6d-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="62f6d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62f6d-110">PARAMETERS</span></span>

### <span data-ttu-id="62f6d-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="62f6d-111">-AsJob</span></span>
<span data-ttu-id="62f6d-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="62f6d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62f6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f6d-113">-DefaultProfile</span></span>
<span data-ttu-id="62f6d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62f6d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f6d-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="62f6d-115">-ExtensionName</span></span>
<span data-ttu-id="62f6d-116">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="62f6d-116">The extension name.</span></span>
<span data-ttu-id="62f6d-117">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="62f6d-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f6d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="62f6d-118">-Force</span></span>
<span data-ttu-id="62f6d-119">Sanal makineden uzantının kaldırılmasını zorlamak için.</span><span class="sxs-lookup"><span data-stu-id="62f6d-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="62f6d-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="62f6d-120">-ForceUpdate</span></span>
<span data-ttu-id="62f6d-121">Zorla güncelleştirmesi için bir etiket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="62f6d-121">Generate a tag for force update.</span></span>  <span data-ttu-id="62f6d-122">Bu, aynı VM 'de yinelenen şifreleme işlemleri gerçekleştirmek için verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="62f6d-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f6d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f6d-123">-ResourceGroupName</span></span>
<span data-ttu-id="62f6d-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="62f6d-124">The resource group name.</span></span>

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

### <span data-ttu-id="62f6d-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="62f6d-125">-VMScaleSetName</span></span>
<span data-ttu-id="62f6d-126">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="62f6d-126">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f6d-127">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="62f6d-127">-VolumeType</span></span>
<span data-ttu-id="62f6d-128">Şifreleme işlemi gerçekleştirmek için birimin türü (OS veya veri)</span><span class="sxs-lookup"><span data-stu-id="62f6d-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f6d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="62f6d-129">-Confirm</span></span>
<span data-ttu-id="62f6d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62f6d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f6d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f6d-131">-WhatIf</span></span>
<span data-ttu-id="62f6d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62f6d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f6d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62f6d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f6d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f6d-134">CommonParameters</span></span>
<span data-ttu-id="62f6d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62f6d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f6d-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62f6d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f6d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62f6d-137">INPUTS</span></span>

### <span data-ttu-id="62f6d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="62f6d-138">System.String</span></span>

### <span data-ttu-id="62f6d-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62f6d-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62f6d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62f6d-140">OUTPUTS</span></span>

### <span data-ttu-id="62f6d-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="62f6d-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="62f6d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62f6d-142">NOTES</span></span>

## <span data-ttu-id="62f6d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62f6d-143">RELATED LINKS</span></span>
