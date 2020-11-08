---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096874"
---
# <span data-ttu-id="d3f20-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d3f20-101">New-AzLogicApp</span></span>

## <span data-ttu-id="d3f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f20-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f20-103">Kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="d3f20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3f20-104">SYNTAX</span></span>

### <span data-ttu-id="d3f20-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f20-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f20-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f20-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3f20-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3f20-107">DESCRIPTION</span></span>
<span data-ttu-id="d3f20-108">**New-Azlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="d3f20-109">Mantık uygulaması, mantık uygulaması tanımında tanımlanan eylemlerin veya tetikleyicilerin koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="d3f20-110">Bu cmdlet bir **Iş akışı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3f20-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="d3f20-111">Bir ad, konum, mantık uygulaması tanımı, kaynak grubu ve plan belirterek bir mantık uygulaması oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3f20-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="d3f20-112">Mantık uygulaması tanımı ve parametreleri JavaScript nesne gösteriminde (JSON) biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="d3f20-113">Tanımlama ve parametreler için şablon olarak bir mantık uygulaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3f20-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="d3f20-114">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d3f20-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d3f20-115">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="d3f20-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d3f20-116">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d3f20-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d3f20-117">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d3f20-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="d3f20-118">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="d3f20-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3f20-119">EXAMPLES</span></span>

### <span data-ttu-id="d3f20-120">Örnek 1: tanım ve parametre dosyası yollarını kullanarak mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d3f20-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="d3f20-121">Bu komut, belirtilen kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="d3f20-122">Mantık uygulaması, dosya yollarının belirttiği tanım ve parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="d3f20-123">Örnek 2: tanım ve parametre nesnelerini kullanarak bir mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d3f20-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="d3f20-124">Bu komut, belirtilen kaynak grubu kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="d3f20-125">Örnek 3: kaynak grubunu belirtmek için ardışık düzeni kullanarak bir mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d3f20-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="d3f20-126">Bu komut, Get-AzResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adındaki kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="d3f20-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d3f20-127">Komut, ardışık düzen işlecini kullanarak o kaynak grubunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3f20-128">Geçerli cmdlet, bu kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="d3f20-129">Mantık uygulaması, dosya yollarının belirttiği tanım ve parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="d3f20-130">Örnek 4: var olan mantık uygulamasına dayalı bir mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d3f20-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="d3f20-131">İlk komut, LogicApp03 adındaki mantık uygulamasını Get-AzLogicApp cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="d3f20-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="d3f20-132">Komut, mantık uygulamasını $Workflow değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d3f20-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="d3f20-133">İkinci komut, $Workflow depolanan mantık uygulamasının tanımını ve parametrelerini kullanan yeni bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f20-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="d3f20-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3f20-134">PARAMETERS</span></span>

### <span data-ttu-id="d3f20-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f20-135">-DefaultProfile</span></span>
<span data-ttu-id="d3f20-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d3f20-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3f20-137">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="d3f20-137">-Definition</span></span>
<span data-ttu-id="d3f20-138">Mantık uygulamanızın tanımını JavaScript nesne gösterimi (JSON) biçiminde bir nesne veya dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="d3f20-139">-DefinitionFilePath</span></span>
<span data-ttu-id="d3f20-140">Bir mantık uygulamasının tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-141">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="d3f20-141">-IntegrationAccountId</span></span>
<span data-ttu-id="d3f20-142">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-142">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-143">-Konum</span><span class="sxs-lookup"><span data-stu-id="d3f20-143">-Location</span></span>
<span data-ttu-id="d3f20-144">Mantık uygulamasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="d3f20-145">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu girin.</span><span class="sxs-lookup"><span data-stu-id="d3f20-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="d3f20-146">Herhangi bir konuma bir mantık uygulaması yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3f20-146">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3f20-147">-Name</span></span>
<span data-ttu-id="d3f20-148">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="d3f20-149">-ParameterFilePath</span></span>
<span data-ttu-id="d3f20-150">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-150">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-151">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="d3f20-151">-Parameters</span></span>
<span data-ttu-id="d3f20-152">Mantık uygulaması için bir parametre koleksiyonu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="d3f20-153">Karma tablo, sözlük \< dizesi \> veya sözlük \< dizesi, WorkflowParameter belirtin \> .</span><span class="sxs-lookup"><span data-stu-id="d3f20-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f20-154">-ResourceGroupName</span></span>
<span data-ttu-id="d3f20-155">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-155">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-156">Durumlu</span><span class="sxs-lookup"><span data-stu-id="d3f20-156">-State</span></span>
<span data-ttu-id="d3f20-157">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="d3f20-158">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="d3f20-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f20-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3f20-159">-Confirm</span></span>
<span data-ttu-id="d3f20-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3f20-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f20-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f20-161">-WhatIf</span></span>
<span data-ttu-id="d3f20-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3f20-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f20-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3f20-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f20-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f20-164">CommonParameters</span></span>
<span data-ttu-id="d3f20-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3f20-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f20-166">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f20-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f20-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3f20-167">INPUTS</span></span>

### <span data-ttu-id="d3f20-168">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f20-168">System.String</span></span>

## <span data-ttu-id="d3f20-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3f20-169">OUTPUTS</span></span>

### <span data-ttu-id="d3f20-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="d3f20-170">System.Object</span></span>

## <span data-ttu-id="d3f20-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3f20-171">NOTES</span></span>

## <span data-ttu-id="d3f20-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3f20-172">RELATED LINKS</span></span>

[<span data-ttu-id="d3f20-173">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="d3f20-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="d3f20-174">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="d3f20-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="d3f20-175">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="d3f20-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="d3f20-176">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="d3f20-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


