---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: e7221c043d8bcb7f88e71c70c14de3a80bd67dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761624"
---
# <span data-ttu-id="be84d-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="be84d-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="be84d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be84d-102">SYNOPSIS</span></span>
<span data-ttu-id="be84d-103">Otomasyon 'da DSC düğüm yapılandırması dağıtım işi zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="be84d-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="be84d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be84d-104">SYNTAX</span></span>

### <span data-ttu-id="be84d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be84d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be84d-106">Byjobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="be84d-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be84d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be84d-107">DESCRIPTION</span></span>
<span data-ttu-id="be84d-108">**Get-AzAutomationDscNodeConfigurationDeployment** cmdlet 'i, Skype Otomasyonu 'NDA bir APS</span><span class="sxs-lookup"><span data-stu-id="be84d-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="be84d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be84d-109">EXAMPLES</span></span>

### <span data-ttu-id="be84d-110">Örnek 1: tüm dağıtım zamanlamalarını alma</span><span class="sxs-lookup"><span data-stu-id="be84d-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="be84d-111">Örnek 2: dağıtım zamanlaması alma</span><span class="sxs-lookup"><span data-stu-id="be84d-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="be84d-112">Yukarıdaki komut, "Config01. Node1" adlı DSC düğüm yapılandırmasını, belirtilen iki boyutlu düğüm adları dizisine dağıtır.</span><span class="sxs-lookup"><span data-stu-id="be84d-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="be84d-113">Dağıtım, aşamalı bir şekilde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="be84d-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="be84d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be84d-114">PARAMETERS</span></span>

### <span data-ttu-id="be84d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be84d-115">-AutomationAccountName</span></span>
<span data-ttu-id="be84d-116">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be84d-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="be84d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be84d-117">-DefaultProfile</span></span>
<span data-ttu-id="be84d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="be84d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be84d-119">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="be84d-119">-JobScheduleId</span></span>
<span data-ttu-id="be84d-120">Var olan bir zamanlanmış dağıtım işinin Iş zamanlaması kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be84d-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be84d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be84d-121">-ResourceGroupName</span></span>
<span data-ttu-id="be84d-122">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be84d-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="be84d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be84d-123">CommonParameters</span></span>
<span data-ttu-id="be84d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be84d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be84d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be84d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be84d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be84d-126">INPUTS</span></span>

### <span data-ttu-id="be84d-127">System. Guid</span><span class="sxs-lookup"><span data-stu-id="be84d-127">System.Guid</span></span>

### <span data-ttu-id="be84d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="be84d-128">System.String</span></span>

## <span data-ttu-id="be84d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be84d-129">OUTPUTS</span></span>

### <span data-ttu-id="be84d-130">Microsoft. Azure. Commands. Automation. model. Nodeconfigurationdeploymentplan</span><span class="sxs-lookup"><span data-stu-id="be84d-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="be84d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be84d-131">NOTES</span></span>

## <span data-ttu-id="be84d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be84d-132">RELATED LINKS</span></span>

[<span data-ttu-id="be84d-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="be84d-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="be84d-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="be84d-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="be84d-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be84d-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="be84d-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be84d-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="be84d-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be84d-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)