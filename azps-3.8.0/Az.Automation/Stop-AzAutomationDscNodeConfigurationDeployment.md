---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095946"
---
# <span data-ttu-id="9ea9e-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9ea9e-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="9ea9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea9e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea9e-103">Otomasyonda DSC düğüm yapılandırma dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="9ea9e-104">Yalnızca geçerli dağıtım işini durdurur, ancak atanmış olan düğüm yapılandırmalarını kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="9ea9e-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ea9e-105">SYNTAX</span></span>

### <span data-ttu-id="9ea9e-106">Byjobıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ea9e-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ea9e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ea9e-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea9e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ea9e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ea9e-109">**Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet 'ı, Azure Otomasyonu 'Nda Istenen durum yapılandırma (DSC) düğümü yapılandırmasının dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="9ea9e-110">Atanmış olması durumunda düğüm gruplarına ödev durdurulur, ancak atanmış olan düğümleri atamamaz.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="9ea9e-111">Zamanlanmış bir işin kaydını kaldırmak için, lütfen mevcut bir zamanlanmış işin atamasını kaldırmak üzere Jobscheduleıd ile [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) 'u kullanın.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="9ea9e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ea9e-112">EXAMPLES</span></span>

### <span data-ttu-id="9ea9e-113">Örnek 1: Otomasyonda Azure DSC düğüm yapılandırmasını dağıtma</span><span class="sxs-lookup"><span data-stu-id="9ea9e-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="9ea9e-114">Yukarıdaki komut, geçirilen JobId ile DSC düğüm yapılandırma dağıtım işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="9ea9e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ea9e-115">PARAMETERS</span></span>

### <span data-ttu-id="9ea9e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ea9e-116">-AutomationAccountName</span></span>
<span data-ttu-id="9ea9e-117">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir</span><span class="sxs-lookup"><span data-stu-id="9ea9e-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="9ea9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea9e-118">-DefaultProfile</span></span>
<span data-ttu-id="9ea9e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9ea9e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ea9e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9ea9e-120">-Force</span></span>
<span data-ttu-id="9ea9e-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="9ea9e-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ea9e-122">-InputObject</span></span>
<span data-ttu-id="9ea9e-123">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="9ea9e-123">Input object for Piping</span></span>

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

### <span data-ttu-id="9ea9e-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="9ea9e-124">-JobId</span></span>
<span data-ttu-id="9ea9e-125">Var olan bir dağıtım işinin Iş kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="9ea9e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9ea9e-126">-PassThru</span></span>
<span data-ttu-id="9ea9e-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ea9e-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ea9e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea9e-129">-ResourceGroupName</span></span>
<span data-ttu-id="9ea9e-130">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="9ea9e-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ea9e-131">-Confirm</span></span>
<span data-ttu-id="9ea9e-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea9e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea9e-133">-WhatIf</span></span>
<span data-ttu-id="9ea9e-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea9e-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea9e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea9e-136">CommonParameters</span></span>
<span data-ttu-id="9ea9e-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ea9e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea9e-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ea9e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea9e-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ea9e-139">INPUTS</span></span>

### <span data-ttu-id="9ea9e-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="9ea9e-140">System.Guid</span></span>

### <span data-ttu-id="9ea9e-141">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9ea9e-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="9ea9e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9ea9e-142">System.String</span></span>

## <span data-ttu-id="9ea9e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ea9e-143">OUTPUTS</span></span>

### <span data-ttu-id="9ea9e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ea9e-144">System.Boolean</span></span>

## <span data-ttu-id="9ea9e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ea9e-145">NOTES</span></span>

## <span data-ttu-id="9ea9e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ea9e-146">RELATED LINKS</span></span>

[<span data-ttu-id="9ea9e-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9ea9e-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="9ea9e-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ea9e-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="9ea9e-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9ea9e-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9ea9e-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9ea9e-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9ea9e-151">Get-Azautomationdscnodeconfigurationdeploymentplan</span><span class="sxs-lookup"><span data-stu-id="9ea9e-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
