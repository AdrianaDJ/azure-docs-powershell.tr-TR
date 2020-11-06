---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 2402591c6c388dbe7c1c6b24a1beb2b298012d4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595016"
---
# <span data-ttu-id="05444-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="05444-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="05444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05444-102">SYNOPSIS</span></span>
<span data-ttu-id="05444-103">VM 'deki Run komutu.</span><span class="sxs-lookup"><span data-stu-id="05444-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05444-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05444-104">SYNTAX</span></span>

### <span data-ttu-id="05444-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05444-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05444-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="05444-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05444-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05444-107">DESCRIPTION</span></span>
<span data-ttu-id="05444-108">VM 'de bir Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="05444-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="05444-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05444-109">EXAMPLES</span></span>

### <span data-ttu-id="05444-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05444-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="05444-111">' sample.ps1 ' betiğini ve ' RgName ' kaynak grubundaki ' VMname ' VM 'sinin parametrelerini geçersiz kılarak RunPowerShellScript 'in Run komutunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="05444-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="05444-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05444-112">PARAMETERS</span></span>

### <span data-ttu-id="05444-113">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="05444-113">-CommandId</span></span>
<span data-ttu-id="05444-114">Run komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="05444-114">The run command id.</span></span>

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

### <span data-ttu-id="05444-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05444-115">-DefaultProfile</span></span>
<span data-ttu-id="05444-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05444-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05444-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="05444-117">-Parameter</span></span>
<span data-ttu-id="05444-118">Run komutu parametreleri.</span><span class="sxs-lookup"><span data-stu-id="05444-118">The run command parameters.</span></span>

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

### <span data-ttu-id="05444-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05444-119">-ResourceGroupName</span></span>
<span data-ttu-id="05444-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="05444-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="05444-121">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="05444-121">-ScriptPath</span></span>
<span data-ttu-id="05444-122">Yürütülecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="05444-122">Path of the script to be executed.</span></span>  <span data-ttu-id="05444-123">Bu değer verildiğinde, verilen komut dosyası komutun varsayılan komut dosyasını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="05444-123">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="05444-124">-VM</span><span class="sxs-lookup"><span data-stu-id="05444-124">-VM</span></span>
<span data-ttu-id="05444-125">PS sanal makine nesnesi.</span><span class="sxs-lookup"><span data-stu-id="05444-125">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="05444-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="05444-126">-VMName</span></span>
<span data-ttu-id="05444-127">Sanal makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="05444-127">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="05444-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="05444-128">-Confirm</span></span>
<span data-ttu-id="05444-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05444-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05444-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05444-130">-WhatIf</span></span>
<span data-ttu-id="05444-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05444-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05444-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05444-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05444-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05444-133">CommonParameters</span></span>
<span data-ttu-id="05444-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05444-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05444-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05444-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05444-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05444-136">INPUTS</span></span>

### <span data-ttu-id="05444-137">System. String</span><span class="sxs-lookup"><span data-stu-id="05444-137">System.String</span></span>
<span data-ttu-id="05444-138">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="05444-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="05444-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05444-139">OUTPUTS</span></span>

### <span data-ttu-id="05444-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="05444-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="05444-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05444-141">NOTES</span></span>

## <span data-ttu-id="05444-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05444-142">RELATED LINKS</span></span>

