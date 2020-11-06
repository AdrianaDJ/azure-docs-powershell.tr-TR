---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 990423db13f13f18f10fb768ac55d2e59b4f2baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595159"
---
# <span data-ttu-id="4189a-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="4189a-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="4189a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4189a-102">SYNOPSIS</span></span>
<span data-ttu-id="4189a-103">Kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4189a-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4189a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4189a-104">SYNTAX</span></span>

### <span data-ttu-id="4189a-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4189a-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4189a-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4189a-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4189a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4189a-107">DESCRIPTION</span></span>
<span data-ttu-id="4189a-108">**New-Azurermlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4189a-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="4189a-109">Mantık uygulaması, mantık uygulaması tanımında tanımlanan eylemlerin veya tetikleyicilerin koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="4189a-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="4189a-110">Bu cmdlet bir **Iş akışı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="4189a-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="4189a-111">Bir ad, konum, mantık uygulaması tanımı, kaynak grubu ve plan belirterek bir mantık uygulaması oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4189a-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="4189a-112">Mantık uygulaması tanımı ve parametreleri JavaScript nesne gösteriminde (JSON) biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="4189a-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="4189a-113">Tanımlama ve parametreler için şablon olarak bir mantık uygulaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4189a-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="4189a-114">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4189a-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4189a-115">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="4189a-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4189a-116">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4189a-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4189a-117">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4189a-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="4189a-118">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="4189a-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="4189a-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4189a-119">EXAMPLES</span></span>

### <span data-ttu-id="4189a-120">Örnek 1: tanım ve parametre dosyası yollarını kullanarak mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4189a-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="4189a-121">Bu komut, belirtilen kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4189a-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="4189a-122">Mantık uygulaması, dosya yollarının belirttiği tanım ve parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="4189a-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="4189a-123">Örnek 2: tanım ve parametre nesnelerini kullanarak bir mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4189a-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="4189a-124">Bu komut, belirtilen kaynak grubu kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4189a-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="4189a-125">Örnek 3: kaynak grubunu belirtmek için ardışık düzeni kullanarak bir mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4189a-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="4189a-126">Bu komut, Get-AzureRmResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adındaki kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="4189a-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="4189a-127">Komut, ardışık düzen işlecini kullanarak o kaynak grubunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="4189a-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4189a-128">Geçerli cmdlet, bu kaynak grubunda bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4189a-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="4189a-129">Mantık uygulaması, dosya yollarının belirttiği tanım ve parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="4189a-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="4189a-130">Örnek 4: var olan mantık uygulamasına dayalı bir mantık uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4189a-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="4189a-131">İlk komut, LogicApp03 adındaki mantık uygulamasını Get-AzureRmLogicApp cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="4189a-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="4189a-132">Komut, mantık uygulamasını $Workflow değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4189a-132">The command stores the logic app in the $Workflow variable.</span></span>

<span data-ttu-id="4189a-133">İkinci komut, $Workflow depolanan mantık uygulamasının tanımını ve parametrelerini kullanan yeni bir mantık uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4189a-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="4189a-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4189a-134">PARAMETERS</span></span>

### <span data-ttu-id="4189a-135">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="4189a-135">-Definition</span></span>
<span data-ttu-id="4189a-136">Mantık uygulamanızın tanımını JavaScript Object Notataion (JSON) biçiminde bir nesne veya dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-136">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4189a-137">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="4189a-137">-DefinitionFilePath</span></span>
<span data-ttu-id="4189a-138">Bir mantık uygulamasının tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-138">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4189a-139">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="4189a-139">-IntegrationAccountId</span></span>
<span data-ttu-id="4189a-140">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-140">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="4189a-141">-Konum</span><span class="sxs-lookup"><span data-stu-id="4189a-141">-Location</span></span>
<span data-ttu-id="4189a-142">Mantık uygulamasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-142">Specifies the location of the logic app.</span></span>
<span data-ttu-id="4189a-143">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu girin.</span><span class="sxs-lookup"><span data-stu-id="4189a-143">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="4189a-144">Herhangi bir konuma bir mantık uygulaması yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4189a-144">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="4189a-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="4189a-145">-Name</span></span>
<span data-ttu-id="4189a-146">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-146">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="4189a-147">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="4189a-147">-ParameterFilePath</span></span>
<span data-ttu-id="4189a-148">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-148">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="4189a-149">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="4189a-149">-Parameters</span></span>
<span data-ttu-id="4189a-150">Mantık uygulaması için bir parametre koleksiyonu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-150">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="4189a-151">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="4189a-151">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="4189a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4189a-152">-ResourceGroupName</span></span>
<span data-ttu-id="4189a-153">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-153">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4189a-154">Durumlu</span><span class="sxs-lookup"><span data-stu-id="4189a-154">-State</span></span>
<span data-ttu-id="4189a-155">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189a-155">Specifies the state of the logic app.</span></span>
<span data-ttu-id="4189a-156">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="4189a-156">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="4189a-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="4189a-157">-Confirm</span></span>
<span data-ttu-id="4189a-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4189a-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4189a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4189a-159">-WhatIf</span></span>
<span data-ttu-id="4189a-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4189a-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4189a-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4189a-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4189a-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4189a-162">-DefaultProfile</span></span>
<span data-ttu-id="4189a-163">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4189a-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4189a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4189a-164">CommonParameters</span></span>
<span data-ttu-id="4189a-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4189a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4189a-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4189a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4189a-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4189a-167">INPUTS</span></span>

### <span data-ttu-id="4189a-168">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4189a-168">None</span></span>

## <span data-ttu-id="4189a-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4189a-169">OUTPUTS</span></span>

### <span data-ttu-id="4189a-170">Microsoft. Azure. Management. Logic. modeller. Workflow</span><span class="sxs-lookup"><span data-stu-id="4189a-170">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="4189a-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4189a-171">NOTES</span></span>

## <span data-ttu-id="4189a-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4189a-172">RELATED LINKS</span></span>

[<span data-ttu-id="4189a-173">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="4189a-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="4189a-174">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="4189a-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="4189a-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="4189a-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="4189a-176">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="4189a-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


