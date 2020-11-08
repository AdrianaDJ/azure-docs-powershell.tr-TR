---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276795"
---
# <span data-ttu-id="a3b5a-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="a3b5a-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="a3b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b5a-103">VM 'de bir komut çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-103">Run a command on the VM.</span></span>

## <span data-ttu-id="a3b5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3b5a-104">SYNTAX</span></span>

### <span data-ttu-id="a3b5a-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3b5a-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b5a-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="a3b5a-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3b5a-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="a3b5a-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3b5a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3b5a-108">DESCRIPTION</span></span>
<span data-ttu-id="a3b5a-109">VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="a3b5a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3b5a-110">EXAMPLES</span></span>

### <span data-ttu-id="a3b5a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3b5a-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="a3b5a-112">' sample.ps1 ' betiğini ve ' RgName ' kaynak grubundaki ' VMname ' VM 'sinin parametrelerini geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="a3b5a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3b5a-113">PARAMETERS</span></span>

### <span data-ttu-id="a3b5a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a3b5a-114">-AsJob</span></span>
<span data-ttu-id="a3b5a-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir iş nesnesi döndürün.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="a3b5a-116">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="a3b5a-116">-CommandId</span></span>
<span data-ttu-id="a3b5a-117">Run komut KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-117">The run command ID.</span></span>

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

### <span data-ttu-id="a3b5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b5a-118">-DefaultProfile</span></span>
<span data-ttu-id="a3b5a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b5a-120">-Parametre</span><span class="sxs-lookup"><span data-stu-id="a3b5a-120">-Parameter</span></span>
<span data-ttu-id="a3b5a-121">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-121">The run command parameters.</span></span>

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

### <span data-ttu-id="a3b5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3b5a-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3b5a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a3b5a-124">-ResourceId</span></span>
<span data-ttu-id="a3b5a-125">VM için kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="a3b5a-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="a3b5a-126">-ScriptPath</span></span>
<span data-ttu-id="a3b5a-127">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-127">Path of the script to be executed.</span></span>  <span data-ttu-id="a3b5a-128">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="a3b5a-129">-VM</span><span class="sxs-lookup"><span data-stu-id="a3b5a-129">-VM</span></span>
<span data-ttu-id="a3b5a-130">PS sanal makine nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b5a-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="a3b5a-131">-VMName</span></span>
<span data-ttu-id="a3b5a-132">Sanal makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="a3b5a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3b5a-133">-Confirm</span></span>
<span data-ttu-id="a3b5a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b5a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b5a-135">-WhatIf</span></span>
<span data-ttu-id="a3b5a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3b5a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b5a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b5a-138">CommonParameters</span></span>
<span data-ttu-id="a3b5a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b5a-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3b5a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b5a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3b5a-141">INPUTS</span></span>

### <span data-ttu-id="a3b5a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b5a-142">System.String</span></span>

### <span data-ttu-id="a3b5a-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a3b5a-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a3b5a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3b5a-144">OUTPUTS</span></span>

### <span data-ttu-id="a3b5a-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="a3b5a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="a3b5a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3b5a-146">NOTES</span></span>

## <span data-ttu-id="a3b5a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3b5a-147">RELATED LINKS</span></span>
