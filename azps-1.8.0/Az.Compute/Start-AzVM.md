---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761215"
---
# <span data-ttu-id="a3846-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-101">Start-AzVM</span></span>

## <span data-ttu-id="a3846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3846-102">SYNOPSIS</span></span>
<span data-ttu-id="a3846-103">Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a3846-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="a3846-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3846-104">SYNTAX</span></span>

### <span data-ttu-id="a3846-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3846-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3846-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="a3846-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3846-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3846-107">DESCRIPTION</span></span>
<span data-ttu-id="a3846-108">**Start-AzVM** cmdlet 'ı bir Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a3846-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="a3846-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3846-109">EXAMPLES</span></span>

### <span data-ttu-id="a3846-110">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="a3846-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a3846-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="a3846-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a3846-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3846-112">PARAMETERS</span></span>

### <span data-ttu-id="a3846-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a3846-113">-AsJob</span></span>
<span data-ttu-id="a3846-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="a3846-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a3846-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3846-115">-DefaultProfile</span></span>
<span data-ttu-id="a3846-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3846-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3846-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a3846-117">-Id</span></span>
<span data-ttu-id="a3846-118">Sanal makinenin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3846-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3846-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3846-119">-Name</span></span>
<span data-ttu-id="a3846-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="a3846-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3846-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3846-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3846-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3846-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3846-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3846-123">-Confirm</span></span>
<span data-ttu-id="a3846-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3846-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3846-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3846-125">-WhatIf</span></span>
<span data-ttu-id="a3846-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3846-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3846-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3846-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3846-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3846-128">CommonParameters</span></span>
<span data-ttu-id="a3846-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3846-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3846-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3846-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3846-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3846-131">INPUTS</span></span>

### <span data-ttu-id="a3846-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a3846-132">System.String</span></span>

## <span data-ttu-id="a3846-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3846-133">OUTPUTS</span></span>

### <span data-ttu-id="a3846-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a3846-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a3846-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3846-135">NOTES</span></span>

## <span data-ttu-id="a3846-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3846-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3846-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a3846-138">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a3846-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a3846-140">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="a3846-141">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a3846-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3846-142">Update-AzVM</span></span>](./Update-AzVM.md)


