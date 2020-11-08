---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096959"
---
# <span data-ttu-id="e0246-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="e0246-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="e0246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0246-102">SYNOPSIS</span></span>
<span data-ttu-id="e0246-103">Sanal makine ölçek kümesi VM 'deki Run komutu.</span><span class="sxs-lookup"><span data-stu-id="e0246-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="e0246-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0246-104">SYNTAX</span></span>

### <span data-ttu-id="e0246-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0246-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0246-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="e0246-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0246-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e0246-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0246-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0246-108">DESCRIPTION</span></span>
<span data-ttu-id="e0246-109">Sanal makine ölçek kümesi VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="e0246-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="e0246-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0246-110">EXAMPLES</span></span>

### <span data-ttu-id="e0246-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0246-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="e0246-112">' sample.ps1 ' komut dosyasını geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın ve ' RgName ' kaynak grubunda yer alan sanal makine ölçeği '</span><span class="sxs-lookup"><span data-stu-id="e0246-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="e0246-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e0246-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="e0246-114">' sample.ps1 ' komut dosyasını geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın ve ' RgName ' kaynak grubunda yer alan sanal makine ölçeği '</span><span class="sxs-lookup"><span data-stu-id="e0246-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="e0246-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0246-115">PARAMETERS</span></span>

### <span data-ttu-id="e0246-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="e0246-116">-AsJob</span></span>
<span data-ttu-id="e0246-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e0246-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0246-118">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="e0246-118">-CommandId</span></span>
<span data-ttu-id="e0246-119">Run komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="e0246-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0246-120">-DefaultProfile</span></span>
<span data-ttu-id="e0246-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0246-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0246-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e0246-122">-InstanceId</span></span>
<span data-ttu-id="e0246-123">Sanal makine ölçek kümesi VM 'sinin örnek KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e0246-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-124">-Parametre</span><span class="sxs-lookup"><span data-stu-id="e0246-124">-Parameter</span></span>
<span data-ttu-id="e0246-125">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="e0246-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0246-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0246-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e0246-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e0246-128">-ResourceId</span></span>
<span data-ttu-id="e0246-129">Sanal makine ölçek kümesi VM 'sinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e0246-129">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="e0246-130">-ScriptPath</span></span>
<span data-ttu-id="e0246-131">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="e0246-131">Path of the script to be executed.</span></span>  <span data-ttu-id="e0246-132">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="e0246-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e0246-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e0246-134">PS sanal makine ölçeği kümesi VM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e0246-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e0246-135">-VMScaleSetName</span></span>
<span data-ttu-id="e0246-136">Sanal makine ölçek kümesi VM 'sinin adı.</span><span class="sxs-lookup"><span data-stu-id="e0246-136">The name of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0246-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0246-137">-Confirm</span></span>
<span data-ttu-id="e0246-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0246-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0246-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0246-139">-WhatIf</span></span>
<span data-ttu-id="e0246-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0246-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0246-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0246-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0246-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0246-142">CommonParameters</span></span>
<span data-ttu-id="e0246-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0246-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0246-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e0246-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0246-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0246-145">INPUTS</span></span>

### <span data-ttu-id="e0246-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e0246-146">System.String</span></span>

### <span data-ttu-id="e0246-147">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e0246-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e0246-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0246-148">OUTPUTS</span></span>

### <span data-ttu-id="e0246-149">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="e0246-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="e0246-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0246-150">NOTES</span></span>

## <span data-ttu-id="e0246-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0246-151">RELATED LINKS</span></span>