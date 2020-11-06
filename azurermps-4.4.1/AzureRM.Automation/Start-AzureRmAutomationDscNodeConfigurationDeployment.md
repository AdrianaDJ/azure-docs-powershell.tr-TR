---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f822f6060827718945f12f998662caeee3b349eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592675"
---
# <span data-ttu-id="bdb84-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb84-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="bdb84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb84-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb84-103">Bir DSC düğüm yapılandırmasını otomatikleştirme 'ye dağıtır.</span><span class="sxs-lookup"><span data-stu-id="bdb84-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdb84-104">SYNTAX</span></span>

### <span data-ttu-id="bdb84-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bdb84-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdb84-106">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="bdb84-106">ByByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdb84-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdb84-107">DESCRIPTION</span></span>
<span data-ttu-id="bdb84-108">**Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet 'ı Azure Otomasyonu 'nda Istenen bir durum yapılandırma (DSC) düğümü yapılandırmasını dağıtımlar.</span><span class="sxs-lookup"><span data-stu-id="bdb84-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="bdb84-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdb84-109">EXAMPLES</span></span>

### <span data-ttu-id="bdb84-110">Örnek 1: Otomasyonda Azure DSC düğüm yapılandırmasını dağıtma</span><span class="sxs-lookup"><span data-stu-id="bdb84-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="bdb84-111">Yukarıdaki komut, "Config01. Node1" adlı DSC düğüm yapılandırmasını, belirtilen iki boyutlu düğüm adları dizisine dağıtır.</span><span class="sxs-lookup"><span data-stu-id="bdb84-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="bdb84-112">Dağıtım, aşamalı bir şekilde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="bdb84-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="bdb84-113">Örnek 2: Otomasyonda Azure DSC düğüm yapılandırma dağıtımını zamanlama</span><span class="sxs-lookup"><span data-stu-id="bdb84-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="bdb84-114">Yukarıdaki komut, "Config01. Node1" adlı bir DSC düğüm yapılandırmasının, sağlanan iki boyutlu düğüm adı dizisine yönelik dağıtımını zamanlar.</span><span class="sxs-lookup"><span data-stu-id="bdb84-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="bdb84-115">Dağıtım, aşamalı bir şekilde gerçekleşir ve zamanlama temelinde yürütülür.</span><span class="sxs-lookup"><span data-stu-id="bdb84-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="bdb84-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdb84-116">PARAMETERS</span></span>

### <span data-ttu-id="bdb84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb84-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdb84-118">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb84-118">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="bdb84-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bdb84-119">-AutomationAccountName</span></span>
<span data-ttu-id="bdb84-120">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb84-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="bdb84-121">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bdb84-121">-NodeConfigurationName</span></span>
<span data-ttu-id="bdb84-122">Bu cmdlet 'in dağıttığı DSC düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb84-122">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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
Parameter Sets: ByByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb84-123">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="bdb84-123">-NodeName</span></span>
<span data-ttu-id="bdb84-124">Düğüm yapılandırmasının dağıtılacağı düğümlerin adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb84-124">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="bdb84-125">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="bdb84-125">-Schedule</span></span>
<span data-ttu-id="bdb84-126">Dağıtım işini zamanlamak için Otomasyon zamanlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bdb84-126">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="bdb84-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bdb84-127">-Force</span></span>
<span data-ttu-id="bdb84-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="bdb84-128">ps_force</span></span>

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

### <span data-ttu-id="bdb84-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bdb84-129">-Confirm</span></span>
<span data-ttu-id="bdb84-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bdb84-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb84-131">-WhatIf</span></span>
<span data-ttu-id="bdb84-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdb84-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb84-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bdb84-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb84-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb84-134">-DefaultProfile</span></span>
<span data-ttu-id="bdb84-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bdb84-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdb84-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdb84-136">-InputObject</span></span>
<span data-ttu-id="bdb84-137">Boru için giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bdb84-137">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb84-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb84-138">CommonParameters</span></span>
<span data-ttu-id="bdb84-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdb84-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb84-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb84-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb84-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdb84-141">INPUTS</span></span>

## <span data-ttu-id="bdb84-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdb84-142">OUTPUTS</span></span>

### <span data-ttu-id="bdb84-143">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb84-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="bdb84-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdb84-144">NOTES</span></span>

## <span data-ttu-id="bdb84-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdb84-145">RELATED LINKS</span></span>

[<span data-ttu-id="bdb84-146">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bdb84-146">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="bdb84-147">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdb84-147">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="bdb84-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb84-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="bdb84-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb84-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="bdb84-150">Get-Azurermautomationdscnodeconfigurationdeploymentzamanlama</span><span class="sxs-lookup"><span data-stu-id="bdb84-150">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="bdb84-151">Yeni-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="bdb84-151">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
