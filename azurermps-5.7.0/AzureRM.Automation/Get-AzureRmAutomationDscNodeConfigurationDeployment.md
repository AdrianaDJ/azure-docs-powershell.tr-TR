---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: d5732058c9bfe077a7241257b4b60865547787e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765115"
---
# <span data-ttu-id="d2ecc-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d2ecc-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="d2ecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ecc-103">Otomasyonda DSC düğüm yapılandırma dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2ecc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2ecc-104">SYNTAX</span></span>

### <span data-ttu-id="d2ecc-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2ecc-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2ecc-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="d2ecc-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ecc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2ecc-107">DESCRIPTION</span></span>
<span data-ttu-id="d2ecc-108">**Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet 'i, Skype Otomasyonu 'NDA bir APS</span><span class="sxs-lookup"><span data-stu-id="d2ecc-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="d2ecc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2ecc-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ecc-110">Örnek 1: düğüm yapılandırma dağıtımını alma</span><span class="sxs-lookup"><span data-stu-id="d2ecc-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="d2ecc-111">Yukarıdaki komut, "Config01. Node1" adlı DSC düğüm yapılandırmasını, belirtilen iki boyutlu düğüm adları dizisine dağıtır.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="d2ecc-112">Dağıtım, aşamalı bir şekilde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="d2ecc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2ecc-113">PARAMETERS</span></span>

### <span data-ttu-id="d2ecc-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2ecc-114">-AutomationAccountName</span></span>
<span data-ttu-id="d2ecc-115">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ecc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ecc-116">-DefaultProfile</span></span>
<span data-ttu-id="d2ecc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d2ecc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ecc-118">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="d2ecc-118">-EndTime</span></span>
<span data-ttu-id="d2ecc-119">Bitiş saati filtresi.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-119">End time filter.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ecc-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="d2ecc-120">-JobId</span></span>
<span data-ttu-id="d2ecc-121">Var olan bir dağıtım işinin Iş kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ecc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ecc-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2ecc-123">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ecc-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d2ecc-124">-StartTime</span></span>
<span data-ttu-id="d2ecc-125">Başlangıç saati filtresi.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-125">Start time filter.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ecc-126">-Durum</span><span class="sxs-lookup"><span data-stu-id="d2ecc-126">-Status</span></span>
<span data-ttu-id="d2ecc-127">Iş filtresinin durumu.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-127">Status of the Job filter.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ecc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ecc-128">CommonParameters</span></span>
<span data-ttu-id="d2ecc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ecc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ecc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ecc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2ecc-131">INPUTS</span></span>

### <span data-ttu-id="d2ecc-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2ecc-132">None</span></span>
<span data-ttu-id="d2ecc-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d2ecc-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2ecc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2ecc-134">OUTPUTS</span></span>

### <span data-ttu-id="d2ecc-135">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d2ecc-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="d2ecc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2ecc-136">NOTES</span></span>

## <span data-ttu-id="d2ecc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2ecc-137">RELATED LINKS</span></span>

[<span data-ttu-id="d2ecc-138">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d2ecc-138">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="d2ecc-139">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2ecc-139">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="d2ecc-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d2ecc-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d2ecc-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d2ecc-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d2ecc-142">Get-Azurermautomationdscnodeconfigurationdeploymentzamanlama</span><span class="sxs-lookup"><span data-stu-id="d2ecc-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
