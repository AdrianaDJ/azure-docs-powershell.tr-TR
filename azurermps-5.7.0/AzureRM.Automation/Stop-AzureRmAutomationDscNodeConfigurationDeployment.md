---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 17106fed79fdec90bad6615560553dcdb5d46703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763586"
---
# <span data-ttu-id="4e962-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4e962-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="4e962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e962-102">SYNOPSIS</span></span>
<span data-ttu-id="4e962-103">Otomasyonda DSC düğüm yapılandırma dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="4e962-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="4e962-104">Yalnızca geçerli dağıtım işini durdurur, ancak atanmış olan düğüm yapılandırmalarını kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="4e962-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e962-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e962-105">SYNTAX</span></span>

### <span data-ttu-id="4e962-106">Byjobıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4e962-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e962-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e962-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e962-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e962-108">DESCRIPTION</span></span>
<span data-ttu-id="4e962-109">**Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet 'ı, Azure Otomasyonu 'Nda Istenen durum yapılandırma (DSC) düğümü yapılandırmasının dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="4e962-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="4e962-110">Atanmış olması durumunda düğüm gruplarına ödev durdurulur, ancak atanmış olan düğümleri atamamaz.</span><span class="sxs-lookup"><span data-stu-id="4e962-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="4e962-111">Zamanlanmış bir işin kaydını kaldırmak için, mevcut bir zamanlanmış işin atamasını kaldırmak üzere Jobscheduleıd ile birlikte [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) 'u kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e962-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="4e962-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e962-112">EXAMPLES</span></span>

### <span data-ttu-id="4e962-113">Örnek 1: Otomasyonda Azure DSC düğüm yapılandırmasını dağıtma</span><span class="sxs-lookup"><span data-stu-id="4e962-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="4e962-114">Yukarıdaki komut, geçirilen JobId ile DSC düğüm yapılandırma dağıtım işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="4e962-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="4e962-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e962-115">PARAMETERS</span></span>

### <span data-ttu-id="4e962-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e962-116">-AutomationAccountName</span></span>
<span data-ttu-id="4e962-117">Bu cmdlet 'in derolduğu DSC yapılandırmasını içeren Otomasyon hesabının adını belirtir</span><span class="sxs-lookup"><span data-stu-id="4e962-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="4e962-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e962-118">-DefaultProfile</span></span>
<span data-ttu-id="4e962-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4e962-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e962-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4e962-120">-Force</span></span>
<span data-ttu-id="4e962-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="4e962-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e962-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e962-122">-InputObject</span></span>
<span data-ttu-id="4e962-123">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="4e962-123">Input object for Piping</span></span>

```yaml
Type: NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e962-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="4e962-124">-JobId</span></span>
<span data-ttu-id="4e962-125">Var olan bir dağıtım işinin Iş kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e962-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="4e962-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4e962-126">-PassThru</span></span>
<span data-ttu-id="4e962-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4e962-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e962-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4e962-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4e962-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e962-129">-ResourceGroupName</span></span>
<span data-ttu-id="4e962-130">Bu cmdlet 'in bir yapılandırmayı derlediğini belirten bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e962-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="4e962-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e962-131">-Confirm</span></span>
<span data-ttu-id="4e962-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e962-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e962-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e962-133">-WhatIf</span></span>
<span data-ttu-id="4e962-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e962-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e962-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e962-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e962-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e962-136">CommonParameters</span></span>
<span data-ttu-id="4e962-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e962-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e962-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e962-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e962-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e962-139">INPUTS</span></span>

### <span data-ttu-id="4e962-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e962-140">None</span></span>
<span data-ttu-id="4e962-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4e962-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e962-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e962-142">OUTPUTS</span></span>

## <span data-ttu-id="4e962-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e962-143">NOTES</span></span>

## <span data-ttu-id="4e962-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e962-144">RELATED LINKS</span></span>

[<span data-ttu-id="4e962-145">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="4e962-145">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="4e962-146">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e962-146">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="4e962-147">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4e962-147">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="4e962-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4e962-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="4e962-149">Get-Azurermautomationdscnodeconfigurationdeploymentzamanlama</span><span class="sxs-lookup"><span data-stu-id="4e962-149">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)