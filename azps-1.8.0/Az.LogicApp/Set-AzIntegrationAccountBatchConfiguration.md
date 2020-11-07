---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 40cd652a957d4e0a7565b573b288b333e4cebe33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915963"
---
# <span data-ttu-id="a64cd-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a64cd-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a64cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a64cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a64cd-103">Tümleştirme hesabı toplu iş yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a64cd-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="a64cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a64cd-104">SYNTAX</span></span>

### <span data-ttu-id="a64cd-105">Byıntegrationaccountandparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a64cd-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-106">Byıntegrationaccountandjson</span><span class="sxs-lookup"><span data-stu-id="a64cd-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-107">Byıntegrationaccountandfilepath</span><span class="sxs-lookup"><span data-stu-id="a64cd-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="a64cd-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a64cd-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="a64cd-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-111">Byresourceıdandjson</span><span class="sxs-lookup"><span data-stu-id="a64cd-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-112">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="a64cd-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64cd-113">Byresourceıdandparameters</span><span class="sxs-lookup"><span data-stu-id="a64cd-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a64cd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="a64cd-114">DESCRIPTION</span></span>
<span data-ttu-id="a64cd-115">**Set-Azıntegrationaccountbatchconfiguration** cmdlet 'i bir tümleştirme hesabı toplu iş yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a64cd-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="a64cd-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a64cd-116">EXAMPLES</span></span>

### <span data-ttu-id="a64cd-117">Örnek 1: yerel dosya kullanarak toplu iş yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a64cd-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a64cd-118">"$BatchConfigurationFilePath" içinde yer alan dosya yolundaki yerel dosyayı kullanarak "sampleBatchConfig" adlı bir toplu iş yapılandırmasını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a64cd-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="a64cd-119">Örnek 2: JSON dizesi kullanarak toplu iş yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a64cd-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a64cd-120">"SampleBatchConfig" adlı bir toplu iş yapılandırmasını değiştirerek "$batchConfigurationContent" içinde bulunan bir JSON dizesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a64cd-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="a64cd-121">Örnek 3: parametreler kullanarak toplu iş yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a64cd-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a64cd-122">Tüm nessecary parametrelerini el ile sağlayarak "sampleBatchConfig" adlı bir toplu iş yapılandırmasını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a64cd-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the nessecary parameters.</span></span>

## <span data-ttu-id="a64cd-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a64cd-123">PARAMETERS</span></span>

### <span data-ttu-id="a64cd-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="a64cd-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="a64cd-125">Tümleştirme hesabı toplu işlem yapılandırma tanımı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="a64cd-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="a64cd-127">Tümleştirme hesabı toplu yapılandırma dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="a64cd-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="a64cd-128">-BatchGroupName</span></span>
<span data-ttu-id="a64cd-129">Tümleştirme hesabı toplu iş Yapılandırması Grup adı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="a64cd-130">-BatchSize</span></span>
<span data-ttu-id="a64cd-131">Tümleştirme hesabı toplu yapılandırması toplu iş boyutu.</span><span class="sxs-lookup"><span data-stu-id="a64cd-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a64cd-132">-DefaultProfile</span></span>
<span data-ttu-id="a64cd-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a64cd-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a64cd-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a64cd-134">-InputObject</span></span>
<span data-ttu-id="a64cd-135">Tümleştirme hesabı toplu iş yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="a64cd-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="a64cd-136">-MessageCount</span></span>
<span data-ttu-id="a64cd-137">Tümleştirme hesabı toplu yapılandırması ileti sayısı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a64cd-138">-Metadata</span></span>
<span data-ttu-id="a64cd-139">Tümleştirme hesabı toplu yapılandırma meta verileri.</span><span class="sxs-lookup"><span data-stu-id="a64cd-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="a64cd-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="a64cd-140">-Name</span></span>
<span data-ttu-id="a64cd-141">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a64cd-142">-ParentName</span></span>
<span data-ttu-id="a64cd-143">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a64cd-144">-ResourceGroupName</span></span>
<span data-ttu-id="a64cd-145">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a64cd-146">-ResourceId</span></span>
<span data-ttu-id="a64cd-147">Tümleştirme hesabı toplu yapılandırması kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a64cd-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="a64cd-148">-ScheduleFrequency</span></span>
<span data-ttu-id="a64cd-149">Tümleştirme hesabı toplu yapılandırması zamanlama sıklığı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-150">-Scheduleınterval</span><span class="sxs-lookup"><span data-stu-id="a64cd-150">-ScheduleInterval</span></span>
<span data-ttu-id="a64cd-151">Tümleştirme hesabı toplu iş yapılandırması zamanlama aralığı.</span><span class="sxs-lookup"><span data-stu-id="a64cd-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="a64cd-152">-ScheduleStartTime</span></span>
<span data-ttu-id="a64cd-153">Tümleştirme hesabı toplu yapılandırması başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="a64cd-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="a64cd-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="a64cd-155">Tümleştirme hesabı toplu iş yapılandırması zamanlama saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="a64cd-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a64cd-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="a64cd-156">-Confirm</span></span>
<span data-ttu-id="a64cd-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a64cd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a64cd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a64cd-158">-WhatIf</span></span>
<span data-ttu-id="a64cd-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a64cd-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a64cd-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a64cd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a64cd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a64cd-161">CommonParameters</span></span>
<span data-ttu-id="a64cd-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a64cd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a64cd-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a64cd-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a64cd-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a64cd-164">INPUTS</span></span>

### <span data-ttu-id="a64cd-165">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="a64cd-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="a64cd-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a64cd-166">System.String</span></span>

## <span data-ttu-id="a64cd-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a64cd-167">OUTPUTS</span></span>

### <span data-ttu-id="a64cd-168">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="a64cd-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a64cd-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a64cd-169">NOTES</span></span>

## <span data-ttu-id="a64cd-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a64cd-170">RELATED LINKS</span></span>