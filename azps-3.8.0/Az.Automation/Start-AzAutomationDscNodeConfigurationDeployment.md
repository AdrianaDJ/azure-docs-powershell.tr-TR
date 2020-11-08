---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096049"
---
# <span data-ttu-id="df008-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df008-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="df008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df008-102">SYNOPSIS</span></span>
<span data-ttu-id="df008-103">Bir DSC düğüm yapılandırmasını otomatikleştirme 'ye dağıtır.</span><span class="sxs-lookup"><span data-stu-id="df008-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="df008-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df008-104">SYNTAX</span></span>

### <span data-ttu-id="df008-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df008-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df008-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df008-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df008-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="df008-107">DESCRIPTION</span></span>
<span data-ttu-id="df008-108">**Start-AzAutomationDscNodeConfigurationDeployment** cmdlet 'ı, Azure Otomasyonu 'nda Istenen bir durum yapılandırma (DSC) düğümü yapılandırmasını dağıtır.</span><span class="sxs-lookup"><span data-stu-id="df008-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="df008-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df008-109">EXAMPLES</span></span>

### <span data-ttu-id="df008-110">Örnek 1: Otomasyonda Azure DSC düğüm yapılandırmasını dağıtma</span><span class="sxs-lookup"><span data-stu-id="df008-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="df008-111">Yukarıdaki komut, "Config01. Node1" adlı DSC düğüm yapılandırmasını, belirtilen iki boyutlu düğüm adları dizisine dağıtır.</span><span class="sxs-lookup"><span data-stu-id="df008-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="df008-112">Dağıtım, aşamalı bir şekilde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="df008-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="df008-113">Örnek 2: Otomasyonda Azure DSC düğüm yapılandırma dağıtımını zamanlama</span><span class="sxs-lookup"><span data-stu-id="df008-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="df008-114">Yukarıdaki komut, "Config01. Node1" adlı bir DSC düğüm yapılandırmasının, sağlanan iki boyutlu düğüm adı dizisine yönelik dağıtımını zamanlar.</span><span class="sxs-lookup"><span data-stu-id="df008-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="df008-115">Dağıtım, aşamalı bir şekilde gerçekleşir ve zamanlama temelinde yürütülür.</span><span class="sxs-lookup"><span data-stu-id="df008-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="df008-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df008-116">PARAMETERS</span></span>

### <span data-ttu-id="df008-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df008-117">-AutomationAccountName</span></span>
<span data-ttu-id="df008-118">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df008-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df008-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df008-119">-DefaultProfile</span></span>
<span data-ttu-id="df008-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df008-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df008-121">-Force</span><span class="sxs-lookup"><span data-stu-id="df008-121">-Force</span></span>
<span data-ttu-id="df008-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="df008-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df008-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df008-123">-InputObject</span></span>
<span data-ttu-id="df008-124">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="df008-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df008-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="df008-125">-NodeConfigurationName</span></span>
<span data-ttu-id="df008-126">Bu cmdlet 'in dağıttığı DSC düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df008-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df008-127">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="df008-127">-NodeName</span></span>
<span data-ttu-id="df008-128">Düğüm yapılandırmasının dağıtılacağı düğümlerin adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df008-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df008-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df008-129">-ResourceGroupName</span></span>
<span data-ttu-id="df008-130">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df008-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="df008-131">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="df008-131">-Schedule</span></span>
<span data-ttu-id="df008-132">Dağıtım işini zamanlamak için Otomasyon zamanlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="df008-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df008-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="df008-133">-Confirm</span></span>
<span data-ttu-id="df008-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df008-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df008-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df008-135">-WhatIf</span></span>
<span data-ttu-id="df008-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df008-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df008-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df008-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df008-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df008-138">CommonParameters</span></span>
<span data-ttu-id="df008-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df008-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df008-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df008-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df008-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df008-141">INPUTS</span></span>

### <span data-ttu-id="df008-142">System. String</span><span class="sxs-lookup"><span data-stu-id="df008-142">System.String</span></span>

### <span data-ttu-id="df008-143">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df008-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="df008-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df008-144">OUTPUTS</span></span>

### <span data-ttu-id="df008-145">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df008-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="df008-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df008-146">NOTES</span></span>

## <span data-ttu-id="df008-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df008-147">RELATED LINKS</span></span>

[<span data-ttu-id="df008-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="df008-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="df008-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="df008-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="df008-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df008-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="df008-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df008-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="df008-152">Get-Azautomationdscnodeconfigurationdeploymentplan</span><span class="sxs-lookup"><span data-stu-id="df008-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="df008-153">Yeni-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="df008-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
