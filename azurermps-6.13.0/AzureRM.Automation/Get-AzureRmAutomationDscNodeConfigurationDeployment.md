---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 0c918328eb0b578eae31994c949210d62eba337b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589604"
---
# <span data-ttu-id="6fa1d-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6fa1d-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="6fa1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fa1d-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa1d-103">Otomasyonda DSC düğüm yapılandırma dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fa1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fa1d-104">SYNTAX</span></span>

### <span data-ttu-id="6fa1d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fa1d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fa1d-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="6fa1d-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fa1d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fa1d-107">DESCRIPTION</span></span>
<span data-ttu-id="6fa1d-108">**Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet 'i, Skype Otomasyonu 'NDA bir APS</span><span class="sxs-lookup"><span data-stu-id="6fa1d-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="6fa1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fa1d-109">EXAMPLES</span></span>

### <span data-ttu-id="6fa1d-110">Örnek 1: düğüm yapılandırma dağıtımını alma</span><span class="sxs-lookup"><span data-stu-id="6fa1d-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="6fa1d-111">Yukarıdaki komut, "Config01. Node1" adlı DSC düğüm yapılandırmasını, belirtilen iki boyutlu düğüm adları dizisine dağıtır.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="6fa1d-112">Dağıtım, aşamalı bir şekilde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="6fa1d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fa1d-113">PARAMETERS</span></span>

### <span data-ttu-id="6fa1d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6fa1d-114">-AutomationAccountName</span></span>
<span data-ttu-id="6fa1d-115">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="6fa1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa1d-116">-DefaultProfile</span></span>
<span data-ttu-id="6fa1d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6fa1d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fa1d-118">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="6fa1d-118">-EndTime</span></span>
<span data-ttu-id="6fa1d-119">Bitiş saati filtresi.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-119">End time filter.</span></span>

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

### <span data-ttu-id="6fa1d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="6fa1d-120">-JobId</span></span>
<span data-ttu-id="6fa1d-121">Var olan bir dağıtım işinin Iş kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="6fa1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6fa1d-123">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="6fa1d-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="6fa1d-124">-StartTime</span></span>
<span data-ttu-id="6fa1d-125">Başlangıç saati filtresi.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-125">Start time filter.</span></span>

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

### <span data-ttu-id="6fa1d-126">-Durum</span><span class="sxs-lookup"><span data-stu-id="6fa1d-126">-Status</span></span>
<span data-ttu-id="6fa1d-127">Iş filtresinin durumu.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="6fa1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa1d-128">CommonParameters</span></span>
<span data-ttu-id="6fa1d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fa1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa1d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa1d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa1d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fa1d-131">INPUTS</span></span>

### <span data-ttu-id="6fa1d-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="6fa1d-132">System.Guid</span></span>

### <span data-ttu-id="6fa1d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6fa1d-133">System.String</span></span>

## <span data-ttu-id="6fa1d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fa1d-134">OUTPUTS</span></span>

### <span data-ttu-id="6fa1d-135">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6fa1d-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="6fa1d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fa1d-136">NOTES</span></span>

## <span data-ttu-id="6fa1d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fa1d-137">RELATED LINKS</span></span>

[<span data-ttu-id="6fa1d-138">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6fa1d-138">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="6fa1d-139">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fa1d-139">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="6fa1d-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6fa1d-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="6fa1d-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6fa1d-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="6fa1d-142">Get-Azurermautomationdscnodeconfigurationdeploymentzamanlama</span><span class="sxs-lookup"><span data-stu-id="6fa1d-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
