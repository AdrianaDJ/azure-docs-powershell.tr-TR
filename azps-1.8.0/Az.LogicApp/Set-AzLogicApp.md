---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 254ab4f1dd126e1b671c9a1d899a9dbe8e71beca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915928"
---
# <span data-ttu-id="93f63-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="93f63-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="93f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f63-102">SYNOPSIS</span></span>
<span data-ttu-id="93f63-103">Kaynak grubundaki bir mantık uygulamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="93f63-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="93f63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93f63-104">SYNTAX</span></span>

### <span data-ttu-id="93f63-105">Tüketim (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93f63-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93f63-106">Hostingplanı</span><span class="sxs-lookup"><span data-stu-id="93f63-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93f63-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93f63-107">DESCRIPTION</span></span>
<span data-ttu-id="93f63-108">**Set-Azlogicuyg** cmdlet 'i, mantık uygulamaları özelliğini kullanarak bir mantık uygulamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="93f63-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="93f63-109">Mantık uygulaması, mantık uygulaması tanımında tanımlanan eylemlerin veya tetikleyicilerin koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="93f63-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="93f63-110">Bu cmdlet bir **Iş akışı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="93f63-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="93f63-111">Bir ad, konum, mantık uygulaması tanımı, kaynak grubu ve plan belirterek bir mantık uygulamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93f63-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="93f63-112">Mantık uygulaması tanımı ve parametreleri JavaScript nesne gösteriminde (JSON) biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="93f63-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="93f63-113">Tanımlama ve parametreler için şablon olarak bir mantık uygulaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93f63-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="93f63-114">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="93f63-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="93f63-115">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="93f63-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="93f63-116">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="93f63-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="93f63-117">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="93f63-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="93f63-118">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="93f63-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="93f63-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93f63-119">EXAMPLES</span></span>

### <span data-ttu-id="93f63-120">Örnek 1: mantık uygulamasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="93f63-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="93f63-121">Bu komut, mantık uygulamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="93f63-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="93f63-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93f63-122">PARAMETERS</span></span>

### <span data-ttu-id="93f63-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93f63-123">-AppServicePlan</span></span>
<span data-ttu-id="93f63-124">Planın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93f63-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f63-125">-DefaultProfile</span></span>
<span data-ttu-id="93f63-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="93f63-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f63-127">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="93f63-127">-Definition</span></span>
<span data-ttu-id="93f63-128">JavaScript nesne gösterimi (JSON) biçiminde bir nesne veya dize olarak bir mantık uygulamasının tanımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="93f63-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="93f63-129">-DefinitionFilePath</span></span>
<span data-ttu-id="93f63-130">Bir mantık uygulamasının tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="93f63-131">-Force</span><span class="sxs-lookup"><span data-stu-id="93f63-131">-Force</span></span>
<span data-ttu-id="93f63-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="93f63-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93f63-133">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="93f63-133">-IntegrationAccountId</span></span>
<span data-ttu-id="93f63-134">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="93f63-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="93f63-135">-Name</span></span>
<span data-ttu-id="93f63-136">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="93f63-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="93f63-137">-ParameterFilePath</span></span>
<span data-ttu-id="93f63-138">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="93f63-139">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="93f63-139">-Parameters</span></span>
<span data-ttu-id="93f63-140">Mantık uygulaması için bir parametre koleksiyonu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="93f63-141">Karma tablo, sözlük \< dizesi \> veya sözlük \< dizesi, WorkflowParameter belirtin \> .</span><span class="sxs-lookup"><span data-stu-id="93f63-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="93f63-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f63-142">-ResourceGroupName</span></span>
<span data-ttu-id="93f63-143">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93f63-144">Durumlu</span><span class="sxs-lookup"><span data-stu-id="93f63-144">-State</span></span>
<span data-ttu-id="93f63-145">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="93f63-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="93f63-146">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="93f63-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="93f63-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="93f63-147">-UseConsumptionModel</span></span>
<span data-ttu-id="93f63-148">Mantık uygulaması faturaının tüketim tabanlı modeli kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93f63-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f63-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="93f63-149">-Confirm</span></span>
<span data-ttu-id="93f63-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93f63-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f63-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f63-151">-WhatIf</span></span>
<span data-ttu-id="93f63-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93f63-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f63-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93f63-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f63-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f63-154">CommonParameters</span></span>
<span data-ttu-id="93f63-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93f63-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f63-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f63-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f63-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93f63-157">INPUTS</span></span>

### <span data-ttu-id="93f63-158">System. String</span><span class="sxs-lookup"><span data-stu-id="93f63-158">System.String</span></span>

## <span data-ttu-id="93f63-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93f63-159">OUTPUTS</span></span>

### <span data-ttu-id="93f63-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="93f63-160">System.Object</span></span>

## <span data-ttu-id="93f63-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93f63-161">NOTES</span></span>

## <span data-ttu-id="93f63-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93f63-162">RELATED LINKS</span></span>

[<span data-ttu-id="93f63-163">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="93f63-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="93f63-164">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="93f63-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="93f63-165">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="93f63-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="93f63-166">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="93f63-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

