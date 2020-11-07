---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764472"
---
# <span data-ttu-id="5160e-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="5160e-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="5160e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5160e-102">SYNOPSIS</span></span>
<span data-ttu-id="5160e-103">VM 'deki Run komutu.</span><span class="sxs-lookup"><span data-stu-id="5160e-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5160e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5160e-104">SYNTAX</span></span>

### <span data-ttu-id="5160e-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5160e-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5160e-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="5160e-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5160e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5160e-107">DESCRIPTION</span></span>
<span data-ttu-id="5160e-108">VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="5160e-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="5160e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5160e-109">EXAMPLES</span></span>

### <span data-ttu-id="5160e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5160e-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="5160e-111">' sample.ps1 ' betiğini ve ' RgName ' kaynak grubundaki ' VMname ' VM 'sinin parametrelerini geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="5160e-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="5160e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5160e-112">PARAMETERS</span></span>

### <span data-ttu-id="5160e-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5160e-113">-AsJob</span></span>
<span data-ttu-id="5160e-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="5160e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5160e-115">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="5160e-115">-CommandId</span></span>
<span data-ttu-id="5160e-116">Run komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="5160e-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5160e-117">-DefaultProfile</span></span>
<span data-ttu-id="5160e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5160e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5160e-119">-Parametre</span><span class="sxs-lookup"><span data-stu-id="5160e-119">-Parameter</span></span>
<span data-ttu-id="5160e-120">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="5160e-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5160e-121">-ResourceGroupName</span></span>
<span data-ttu-id="5160e-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5160e-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="5160e-123">-ScriptPath</span></span>
<span data-ttu-id="5160e-124">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="5160e-124">Path of the script to be executed.</span></span>  <span data-ttu-id="5160e-125">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="5160e-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-126">-VM</span><span class="sxs-lookup"><span data-stu-id="5160e-126">-VM</span></span>
<span data-ttu-id="5160e-127">PS sanal makine nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5160e-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="5160e-128">-VMName</span></span>
<span data-ttu-id="5160e-129">Sanal makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="5160e-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="5160e-130">-Confirm</span></span>
<span data-ttu-id="5160e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5160e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5160e-132">-WhatIf</span></span>
<span data-ttu-id="5160e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5160e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5160e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5160e-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5160e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5160e-135">CommonParameters</span></span>
<span data-ttu-id="5160e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5160e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5160e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5160e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5160e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5160e-138">INPUTS</span></span>

### <span data-ttu-id="5160e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5160e-139">System.String</span></span>
<span data-ttu-id="5160e-140">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5160e-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5160e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5160e-141">OUTPUTS</span></span>

### <span data-ttu-id="5160e-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="5160e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="5160e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5160e-143">NOTES</span></span>

## <span data-ttu-id="5160e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5160e-144">RELATED LINKS</span></span>
