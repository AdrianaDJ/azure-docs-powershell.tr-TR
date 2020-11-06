---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590367"
---
# <span data-ttu-id="ce56d-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ce56d-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="ce56d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce56d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce56d-103">VM 'deki Run komutu.</span><span class="sxs-lookup"><span data-stu-id="ce56d-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce56d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce56d-104">SYNTAX</span></span>

### <span data-ttu-id="ce56d-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce56d-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce56d-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="ce56d-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce56d-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="ce56d-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce56d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce56d-108">DESCRIPTION</span></span>
<span data-ttu-id="ce56d-109">VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="ce56d-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="ce56d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce56d-110">EXAMPLES</span></span>

### <span data-ttu-id="ce56d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ce56d-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="ce56d-112">' sample.ps1 ' betiğini ve ' RgName ' kaynak grubundaki ' VMname ' VM 'sinin parametrelerini geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="ce56d-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="ce56d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce56d-113">PARAMETERS</span></span>

### <span data-ttu-id="ce56d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ce56d-114">-AsJob</span></span>
<span data-ttu-id="ce56d-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="ce56d-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ce56d-116">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="ce56d-116">-CommandId</span></span>
<span data-ttu-id="ce56d-117">Run komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="ce56d-117">The run command id.</span></span>

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

### <span data-ttu-id="ce56d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce56d-118">-DefaultProfile</span></span>
<span data-ttu-id="ce56d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce56d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce56d-120">-Parametre</span><span class="sxs-lookup"><span data-stu-id="ce56d-120">-Parameter</span></span>
<span data-ttu-id="ce56d-121">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="ce56d-121">The run command parameters.</span></span>

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

### <span data-ttu-id="ce56d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce56d-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce56d-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ce56d-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce56d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ce56d-124">-ResourceId</span></span>
<span data-ttu-id="ce56d-125">VM için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ce56d-125">The resource id for the VM</span></span>

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

### <span data-ttu-id="ce56d-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="ce56d-126">-ScriptPath</span></span>
<span data-ttu-id="ce56d-127">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="ce56d-127">Path of the script to be executed.</span></span>  <span data-ttu-id="ce56d-128">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="ce56d-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="ce56d-129">-VM</span><span class="sxs-lookup"><span data-stu-id="ce56d-129">-VM</span></span>
<span data-ttu-id="ce56d-130">PS sanal makine nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ce56d-130">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="ce56d-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="ce56d-131">-VMName</span></span>
<span data-ttu-id="ce56d-132">Sanal makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="ce56d-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce56d-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce56d-133">-Confirm</span></span>
<span data-ttu-id="ce56d-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce56d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce56d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce56d-135">-WhatIf</span></span>
<span data-ttu-id="ce56d-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce56d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce56d-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce56d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce56d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce56d-138">CommonParameters</span></span>
<span data-ttu-id="ce56d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce56d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce56d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce56d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce56d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce56d-141">INPUTS</span></span>

### <span data-ttu-id="ce56d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ce56d-142">System.String</span></span>

### <span data-ttu-id="ce56d-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ce56d-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ce56d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce56d-144">OUTPUTS</span></span>

### <span data-ttu-id="ce56d-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="ce56d-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="ce56d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce56d-146">NOTES</span></span>

## <span data-ttu-id="ce56d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce56d-147">RELATED LINKS</span></span>
