---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267155"
---
# <span data-ttu-id="b02b9-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b02b9-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="b02b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b02b9-103">Tümleştirme hesabı toplu iş yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b02b9-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="b02b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b02b9-104">SYNTAX</span></span>

### <span data-ttu-id="b02b9-105">Byıntegrationaccountandparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b02b9-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-106">Byıntegrationaccountandjson</span><span class="sxs-lookup"><span data-stu-id="b02b9-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-107">Byıntegrationaccountandfilepath</span><span class="sxs-lookup"><span data-stu-id="b02b9-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="b02b9-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="b02b9-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="b02b9-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-111">Byresourceıdandjson</span><span class="sxs-lookup"><span data-stu-id="b02b9-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-112">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="b02b9-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02b9-113">Byresourceıdandparameters</span><span class="sxs-lookup"><span data-stu-id="b02b9-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02b9-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="b02b9-114">DESCRIPTION</span></span>
<span data-ttu-id="b02b9-115">**Set-Azıntegrationaccountbatchconfiguration** cmdlet 'i bir tümleştirme hesabı toplu iş yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b02b9-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="b02b9-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b02b9-116">EXAMPLES</span></span>

### <span data-ttu-id="b02b9-117">Örnek 1: yerel dosya kullanarak toplu iş yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b02b9-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b02b9-118">"$BatchConfigurationFilePath" içinde yer alan dosya yolundaki yerel dosyayı kullanarak "sampleBatchConfig" adlı bir toplu iş yapılandırmasını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b02b9-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="b02b9-119">Örnek 2: JSON dizesi kullanarak toplu iş yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b02b9-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b02b9-120">"SampleBatchConfig" adlı bir toplu iş yapılandırmasını değiştirerek "$batchConfigurationContent" içinde bulunan bir JSON dizesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b02b9-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="b02b9-121">Örnek 3: parametreler kullanarak toplu iş yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b02b9-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b02b9-122">Gerekli parametrelerin tümünü el ile sağlayarak "sampleBatchConfig" adlı bir toplu iş yapılandırmasını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b02b9-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="b02b9-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b02b9-123">PARAMETERS</span></span>

### <span data-ttu-id="b02b9-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="b02b9-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="b02b9-125">Tümleştirme hesabı toplu işlem yapılandırma tanımı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="b02b9-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="b02b9-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="b02b9-127">Tümleştirme hesabı toplu yapılandırma dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="b02b9-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="b02b9-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="b02b9-128">-BatchGroupName</span></span>
<span data-ttu-id="b02b9-129">Tümleştirme hesabı toplu iş Yapılandırması Grup adı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="b02b9-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="b02b9-130">-BatchSize</span></span>
<span data-ttu-id="b02b9-131">Tümleştirme hesabı toplu yapılandırması toplu iş boyutu.</span><span class="sxs-lookup"><span data-stu-id="b02b9-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="b02b9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02b9-132">-DefaultProfile</span></span>
<span data-ttu-id="b02b9-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b02b9-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b02b9-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b02b9-134">-InputObject</span></span>
<span data-ttu-id="b02b9-135">Tümleştirme hesabı toplu iş yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="b02b9-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="b02b9-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="b02b9-136">-MessageCount</span></span>
<span data-ttu-id="b02b9-137">Tümleştirme hesabı toplu yapılandırması ileti sayısı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="b02b9-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b02b9-138">-Metadata</span></span>
<span data-ttu-id="b02b9-139">Tümleştirme hesabı toplu yapılandırma meta verileri.</span><span class="sxs-lookup"><span data-stu-id="b02b9-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="b02b9-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="b02b9-140">-Name</span></span>
<span data-ttu-id="b02b9-141">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="b02b9-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="b02b9-142">-ParentName</span></span>
<span data-ttu-id="b02b9-143">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-143">The integration account name.</span></span>

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

### <span data-ttu-id="b02b9-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02b9-144">-ResourceGroupName</span></span>
<span data-ttu-id="b02b9-145">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-145">The resource group name.</span></span>

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

### <span data-ttu-id="b02b9-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b02b9-146">-ResourceId</span></span>
<span data-ttu-id="b02b9-147">Tümleştirme hesabı toplu yapılandırması kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b02b9-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="b02b9-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="b02b9-148">-ScheduleFrequency</span></span>
<span data-ttu-id="b02b9-149">Tümleştirme hesabı toplu yapılandırması zamanlama sıklığı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="b02b9-150">-Scheduleınterval</span><span class="sxs-lookup"><span data-stu-id="b02b9-150">-ScheduleInterval</span></span>
<span data-ttu-id="b02b9-151">Tümleştirme hesabı toplu iş yapılandırması zamanlama aralığı.</span><span class="sxs-lookup"><span data-stu-id="b02b9-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="b02b9-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="b02b9-152">-ScheduleStartTime</span></span>
<span data-ttu-id="b02b9-153">Tümleştirme hesabı toplu yapılandırması başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="b02b9-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="b02b9-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="b02b9-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="b02b9-155">Tümleştirme hesabı toplu iş yapılandırması zamanlama saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="b02b9-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="b02b9-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="b02b9-156">-Confirm</span></span>
<span data-ttu-id="b02b9-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b02b9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02b9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02b9-158">-WhatIf</span></span>
<span data-ttu-id="b02b9-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b02b9-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b02b9-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b02b9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02b9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02b9-161">CommonParameters</span></span>
<span data-ttu-id="b02b9-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b02b9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02b9-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02b9-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02b9-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b02b9-164">INPUTS</span></span>

### <span data-ttu-id="b02b9-165">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="b02b9-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="b02b9-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b02b9-166">System.String</span></span>

## <span data-ttu-id="b02b9-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b02b9-167">OUTPUTS</span></span>

### <span data-ttu-id="b02b9-168">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="b02b9-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="b02b9-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b02b9-169">NOTES</span></span>

## <span data-ttu-id="b02b9-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b02b9-170">RELATED LINKS</span></span>
