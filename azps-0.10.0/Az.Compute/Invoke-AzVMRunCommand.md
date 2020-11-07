---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 3036b26c4f3ebe6fc6f039f1754acdb3b50977f6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936982"
---
# <span data-ttu-id="ecbab-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ecbab-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="ecbab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecbab-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbab-103">VM 'deki Run komutu.</span><span class="sxs-lookup"><span data-stu-id="ecbab-103">Run command on the VM.</span></span>

## <span data-ttu-id="ecbab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecbab-104">SYNTAX</span></span>

### <span data-ttu-id="ecbab-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ecbab-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbab-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="ecbab-106">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecbab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecbab-107">DESCRIPTION</span></span>
<span data-ttu-id="ecbab-108">VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="ecbab-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="ecbab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecbab-109">EXAMPLES</span></span>

### <span data-ttu-id="ecbab-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ecbab-110">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="ecbab-111">' sample.ps1 ' betiğini ve ' RgName ' kaynak grubundaki ' VMname ' VM 'sinin parametrelerini geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="ecbab-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="ecbab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecbab-112">PARAMETERS</span></span>

### <span data-ttu-id="ecbab-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ecbab-113">-AsJob</span></span>
<span data-ttu-id="ecbab-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="ecbab-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ecbab-115">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="ecbab-115">-CommandId</span></span>
<span data-ttu-id="ecbab-116">Run komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="ecbab-116">The run command id.</span></span>

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

### <span data-ttu-id="ecbab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbab-117">-DefaultProfile</span></span>
<span data-ttu-id="ecbab-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ecbab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecbab-119">-Parametre</span><span class="sxs-lookup"><span data-stu-id="ecbab-119">-Parameter</span></span>
<span data-ttu-id="ecbab-120">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="ecbab-120">The run command parameters.</span></span>

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

### <span data-ttu-id="ecbab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbab-121">-ResourceGroupName</span></span>
<span data-ttu-id="ecbab-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ecbab-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecbab-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="ecbab-123">-ScriptPath</span></span>
<span data-ttu-id="ecbab-124">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="ecbab-124">Path of the script to be executed.</span></span>  <span data-ttu-id="ecbab-125">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="ecbab-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="ecbab-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ecbab-126">-VM</span></span>
<span data-ttu-id="ecbab-127">PS sanal makine nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ecbab-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="ecbab-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="ecbab-128">-VMName</span></span>
<span data-ttu-id="ecbab-129">Sanal makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="ecbab-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="ecbab-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ecbab-130">-Confirm</span></span>
<span data-ttu-id="ecbab-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ecbab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecbab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecbab-132">-WhatIf</span></span>
<span data-ttu-id="ecbab-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ecbab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecbab-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ecbab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecbab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbab-135">CommonParameters</span></span>
<span data-ttu-id="ecbab-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecbab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbab-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecbab-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbab-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecbab-138">INPUTS</span></span>

### <span data-ttu-id="ecbab-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ecbab-139">System.String</span></span>
<span data-ttu-id="ecbab-140">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ecbab-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ecbab-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecbab-141">OUTPUTS</span></span>

### <span data-ttu-id="ecbab-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="ecbab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="ecbab-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecbab-143">NOTES</span></span>

## <span data-ttu-id="ecbab-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecbab-144">RELATED LINKS</span></span>

