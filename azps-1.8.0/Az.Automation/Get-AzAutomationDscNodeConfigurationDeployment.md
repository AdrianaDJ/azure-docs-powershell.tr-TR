---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 74966351f50be86f19441edc254af227f2e17fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761625"
---
# <span data-ttu-id="af7aa-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="af7aa-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="af7aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="af7aa-103">Otomasyonda DSC düğüm yapılandırma dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="af7aa-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="af7aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af7aa-104">SYNTAX</span></span>

### <span data-ttu-id="af7aa-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af7aa-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7aa-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="af7aa-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af7aa-107">DESCRIPTION</span></span>
<span data-ttu-id="af7aa-108">**Get-AzAutomationDscNodeConfigurationDeployment** cmdlet 'i, Skype Otomasyonu 'NDA bir APS</span><span class="sxs-lookup"><span data-stu-id="af7aa-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="af7aa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af7aa-109">EXAMPLES</span></span>

### <span data-ttu-id="af7aa-110">Örnek 1: düğüm yapılandırma dağıtımını alma</span><span class="sxs-lookup"><span data-stu-id="af7aa-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="af7aa-111">Yukarıdaki komut, "Config01. Node1" adlı DSC düğüm yapılandırmasını, belirtilen iki boyutlu düğüm adları dizisine dağıtır.</span><span class="sxs-lookup"><span data-stu-id="af7aa-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="af7aa-112">Dağıtım, aşamalı bir şekilde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="af7aa-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="af7aa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af7aa-113">PARAMETERS</span></span>

### <span data-ttu-id="af7aa-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af7aa-114">-AutomationAccountName</span></span>
<span data-ttu-id="af7aa-115">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af7aa-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="af7aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7aa-116">-DefaultProfile</span></span>
<span data-ttu-id="af7aa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="af7aa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af7aa-118">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="af7aa-118">-EndTime</span></span>
<span data-ttu-id="af7aa-119">Bitiş saati filtresi.</span><span class="sxs-lookup"><span data-stu-id="af7aa-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7aa-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="af7aa-120">-JobId</span></span>
<span data-ttu-id="af7aa-121">Var olan bir dağıtım işinin Iş kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af7aa-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af7aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="af7aa-123">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af7aa-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="af7aa-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="af7aa-124">-StartTime</span></span>
<span data-ttu-id="af7aa-125">Başlangıç saati filtresi.</span><span class="sxs-lookup"><span data-stu-id="af7aa-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7aa-126">-Durum</span><span class="sxs-lookup"><span data-stu-id="af7aa-126">-Status</span></span>
<span data-ttu-id="af7aa-127">Iş filtresinin durumu.</span><span class="sxs-lookup"><span data-stu-id="af7aa-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7aa-128">CommonParameters</span></span>
<span data-ttu-id="af7aa-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af7aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7aa-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7aa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7aa-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af7aa-131">INPUTS</span></span>

### <span data-ttu-id="af7aa-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="af7aa-132">System.Guid</span></span>

### <span data-ttu-id="af7aa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="af7aa-133">System.String</span></span>

## <span data-ttu-id="af7aa-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af7aa-134">OUTPUTS</span></span>

### <span data-ttu-id="af7aa-135">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="af7aa-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="af7aa-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af7aa-136">NOTES</span></span>

## <span data-ttu-id="af7aa-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af7aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="af7aa-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="af7aa-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="af7aa-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7aa-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="af7aa-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="af7aa-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="af7aa-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="af7aa-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="af7aa-142">Get-Azautomationdscnodeconfigurationdeploymentplan</span><span class="sxs-lookup"><span data-stu-id="af7aa-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
