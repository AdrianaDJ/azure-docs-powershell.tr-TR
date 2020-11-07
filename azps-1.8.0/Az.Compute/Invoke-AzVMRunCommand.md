---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: c0b61ffa8e973787e27e343d8bcc41c81373414a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761323"
---
# <span data-ttu-id="6f4a9-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6f4a9-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="6f4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6f4a9-103">VM 'de bir komut çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-103">Run a command on the VM.</span></span>

## <span data-ttu-id="6f4a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f4a9-104">SYNTAX</span></span>

### <span data-ttu-id="6f4a9-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f4a9-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f4a9-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="6f4a9-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f4a9-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="6f4a9-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f4a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f4a9-108">DESCRIPTION</span></span>
<span data-ttu-id="6f4a9-109">VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="6f4a9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f4a9-110">EXAMPLES</span></span>

### <span data-ttu-id="6f4a9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f4a9-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="6f4a9-112">' sample.ps1 ' betiğini ve ' RgName ' kaynak grubundaki ' VMname ' VM 'sinin parametrelerini geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="6f4a9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f4a9-113">PARAMETERS</span></span>

### <span data-ttu-id="6f4a9-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6f4a9-114">-AsJob</span></span>
<span data-ttu-id="6f4a9-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir iş nesnesi döndürün.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="6f4a9-116">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="6f4a9-116">-CommandId</span></span>
<span data-ttu-id="6f4a9-117">Run komut KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-117">The run command ID.</span></span>

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

### <span data-ttu-id="6f4a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f4a9-118">-DefaultProfile</span></span>
<span data-ttu-id="6f4a9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f4a9-120">-Parametre</span><span class="sxs-lookup"><span data-stu-id="6f4a9-120">-Parameter</span></span>
<span data-ttu-id="6f4a9-121">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-121">The run command parameters.</span></span>

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

### <span data-ttu-id="6f4a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f4a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f4a9-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f4a9-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6f4a9-124">-ResourceId</span></span>
<span data-ttu-id="6f4a9-125">VM için kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="6f4a9-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="6f4a9-126">-ScriptPath</span></span>
<span data-ttu-id="6f4a9-127">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-127">Path of the script to be executed.</span></span>  <span data-ttu-id="6f4a9-128">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="6f4a9-129">-VM</span><span class="sxs-lookup"><span data-stu-id="6f4a9-129">-VM</span></span>
<span data-ttu-id="6f4a9-130">PS sanal makine nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-130">The PS virtual machine object.</span></span>

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

### <span data-ttu-id="6f4a9-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f4a9-131">-VMName</span></span>
<span data-ttu-id="6f4a9-132">Sanal makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="6f4a9-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f4a9-133">-Confirm</span></span>
<span data-ttu-id="6f4a9-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f4a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f4a9-135">-WhatIf</span></span>
<span data-ttu-id="6f4a9-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f4a9-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f4a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f4a9-138">CommonParameters</span></span>
<span data-ttu-id="6f4a9-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f4a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f4a9-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f4a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f4a9-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f4a9-141">INPUTS</span></span>

### <span data-ttu-id="6f4a9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6f4a9-142">System.String</span></span>

### <span data-ttu-id="6f4a9-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6f4a9-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6f4a9-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f4a9-144">OUTPUTS</span></span>

### <span data-ttu-id="6f4a9-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="6f4a9-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="6f4a9-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f4a9-146">NOTES</span></span>

## <span data-ttu-id="6f4a9-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f4a9-147">RELATED LINKS</span></span>
