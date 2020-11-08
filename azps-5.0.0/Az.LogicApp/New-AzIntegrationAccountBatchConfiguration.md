---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280148"
---
# <span data-ttu-id="b4805-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4805-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="b4805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4805-102">SYNOPSIS</span></span>
<span data-ttu-id="b4805-103">Tümleştirme hesabı toplu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4805-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="b4805-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4805-104">SYNTAX</span></span>

### <span data-ttu-id="b4805-105">Byıntegrationaccountandparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4805-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-106">Byıntegrationaccountandjson</span><span class="sxs-lookup"><span data-stu-id="b4805-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-107">Byıntegrationaccountandfilepath</span><span class="sxs-lookup"><span data-stu-id="b4805-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="b4805-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="b4805-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="b4805-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-111">Byresourceıdandjson</span><span class="sxs-lookup"><span data-stu-id="b4805-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-112">Byresourceıdandfilepath</span><span class="sxs-lookup"><span data-stu-id="b4805-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4805-113">Byresourceıdandparameters</span><span class="sxs-lookup"><span data-stu-id="b4805-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4805-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4805-114">DESCRIPTION</span></span>
<span data-ttu-id="b4805-115">**Get-Azıntegrationaccountbatchconfiguration** cmdlet 'i, tümleştirme hesabında yeni bir toplu iş yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4805-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="b4805-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4805-116">EXAMPLES</span></span>

### <span data-ttu-id="b4805-117">Örnek 1: yerel dosya kullanarak yeni toplu iş yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4805-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b4805-118">"$BatchConfigurationFilePath" içinde yer alan dosya yolundaki yerel dosyayı kullanarak yeni bir toplu iş yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4805-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="b4805-119">Örnek 2: JSON dizesi kullanarak yeni toplu iş yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4805-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b4805-120">"$BatchConfigurationContent" içinde bulunan bir JSON dizesini kullanarak yeni bir toplu iş yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4805-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="b4805-121">Örnek 3: parametreler kullanarak yeni toplu iş yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4805-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b4805-122">Gerekli parametrelerin tümünü el ile sağlayarak yeni bir toplu iş yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4805-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="b4805-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4805-123">PARAMETERS</span></span>

### <span data-ttu-id="b4805-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="b4805-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="b4805-125">Tümleştirme hesabı toplu işlem yapılandırma tanımı.</span><span class="sxs-lookup"><span data-stu-id="b4805-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="b4805-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="b4805-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="b4805-127">Tümleştirme hesabı toplu yapılandırma dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="b4805-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="b4805-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="b4805-128">-BatchGroupName</span></span>
<span data-ttu-id="b4805-129">Tümleştirme hesabı toplu iş Yapılandırması Grup adı.</span><span class="sxs-lookup"><span data-stu-id="b4805-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="b4805-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="b4805-130">-BatchSize</span></span>
<span data-ttu-id="b4805-131">Tümleştirme hesabı toplu yapılandırması toplu iş boyutu.</span><span class="sxs-lookup"><span data-stu-id="b4805-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="b4805-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4805-132">-DefaultProfile</span></span>
<span data-ttu-id="b4805-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4805-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4805-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="b4805-134">-MessageCount</span></span>
<span data-ttu-id="b4805-135">Tümleştirme hesabı toplu yapılandırması ileti sayısı.</span><span class="sxs-lookup"><span data-stu-id="b4805-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="b4805-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b4805-136">-Metadata</span></span>
<span data-ttu-id="b4805-137">Tümleştirme hesabı toplu yapılandırma meta verileri.</span><span class="sxs-lookup"><span data-stu-id="b4805-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="b4805-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4805-138">-Name</span></span>
<span data-ttu-id="b4805-139">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="b4805-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4805-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="b4805-140">-ParentName</span></span>
<span data-ttu-id="b4805-141">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b4805-141">The integration account name.</span></span>

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

### <span data-ttu-id="b4805-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4805-142">-ParentObject</span></span>
<span data-ttu-id="b4805-143">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b4805-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4805-144">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4805-144">-ParentResourceId</span></span>
<span data-ttu-id="b4805-145">Tümleştirme hesabı toplu yapılandırması kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b4805-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="b4805-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4805-146">-ResourceGroupName</span></span>
<span data-ttu-id="b4805-147">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4805-147">The resource group name.</span></span>

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

### <span data-ttu-id="b4805-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="b4805-148">-ScheduleFrequency</span></span>
<span data-ttu-id="b4805-149">Tümleştirme hesabı toplu yapılandırması zamanlama sıklığı.</span><span class="sxs-lookup"><span data-stu-id="b4805-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="b4805-150">-Scheduleınterval</span><span class="sxs-lookup"><span data-stu-id="b4805-150">-ScheduleInterval</span></span>
<span data-ttu-id="b4805-151">Tümleştirme hesabı toplu iş yapılandırması zamanlama aralığı.</span><span class="sxs-lookup"><span data-stu-id="b4805-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="b4805-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="b4805-152">-ScheduleStartTime</span></span>
<span data-ttu-id="b4805-153">Tümleştirme hesabı toplu yapılandırması başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="b4805-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="b4805-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="b4805-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="b4805-155">Tümleştirme hesabı toplu iş yapılandırması zamanlama saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="b4805-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="b4805-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4805-156">-Confirm</span></span>
<span data-ttu-id="b4805-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4805-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4805-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4805-158">-WhatIf</span></span>
<span data-ttu-id="b4805-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4805-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4805-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4805-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4805-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4805-161">CommonParameters</span></span>
<span data-ttu-id="b4805-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4805-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4805-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4805-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4805-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4805-164">INPUTS</span></span>

### <span data-ttu-id="b4805-165">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="b4805-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="b4805-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b4805-166">System.String</span></span>

## <span data-ttu-id="b4805-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4805-167">OUTPUTS</span></span>

### <span data-ttu-id="b4805-168">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="b4805-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="b4805-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4805-169">NOTES</span></span>

## <span data-ttu-id="b4805-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4805-170">RELATED LINKS</span></span>
