---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: 1f98fb17f6dc5604dfd19faeb9b9d6ec54e859c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764994"
---
# <span data-ttu-id="09ae8-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="09ae8-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="09ae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="09ae8-103">Kaynak grubundaki bir mantık uygulamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ae8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09ae8-104">SYNTAX</span></span>

### <span data-ttu-id="09ae8-105">Tüketim (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="09ae8-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09ae8-106">Hostingplanı</span><span class="sxs-lookup"><span data-stu-id="09ae8-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09ae8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09ae8-107">DESCRIPTION</span></span>
<span data-ttu-id="09ae8-108">**Set-Azurermlogicuyg** cmdlet 'i, mantık uygulamaları özelliğini kullanarak bir mantık uygulamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="09ae8-109">Mantık uygulaması, mantık uygulaması tanımında tanımlanan eylemlerin veya tetikleyicilerin koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="09ae8-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="09ae8-110">Bu cmdlet bir **Iş akışı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="09ae8-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="09ae8-111">Bir ad, konum, mantık uygulaması tanımı, kaynak grubu ve plan belirterek bir mantık uygulamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ae8-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="09ae8-112">Mantık uygulaması tanımı ve parametreleri JavaScript nesne gösteriminde (JSON) biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="09ae8-113">Tanımlama ve parametreler için şablon olarak bir mantık uygulaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ae8-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="09ae8-114">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="09ae8-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="09ae8-115">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="09ae8-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="09ae8-116">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="09ae8-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="09ae8-117">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="09ae8-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="09ae8-118">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="09ae8-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09ae8-119">EXAMPLES</span></span>

### <span data-ttu-id="09ae8-120">Örnek 1: mantık uygulamasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="09ae8-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="09ae8-121">Bu komut, mantık uygulamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="09ae8-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09ae8-122">PARAMETERS</span></span>

### <span data-ttu-id="09ae8-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09ae8-123">-AppServicePlan</span></span>
<span data-ttu-id="09ae8-124">Planın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-124">Specifies the name of a plan.</span></span>

```yaml
Type: String
Parameter Sets: HostingPlan
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ae8-125">-DefaultProfile</span></span>
<span data-ttu-id="09ae8-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="09ae8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09ae8-127">Tanımlı</span><span class="sxs-lookup"><span data-stu-id="09ae8-127">-Definition</span></span>
<span data-ttu-id="09ae8-128">JavaScript nesne gösterimi (JSON) biçiminde bir nesne veya dize olarak bir mantık uygulamasının tanımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="09ae8-129">-DefinitionFilePath</span></span>
<span data-ttu-id="09ae8-130">Bir mantık uygulamasının tanımını JSON biçimindeki bir tanım dosyasının yolu olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-131">-Force</span><span class="sxs-lookup"><span data-stu-id="09ae8-131">-Force</span></span>
<span data-ttu-id="09ae8-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="09ae8-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09ae8-133">-Integrationaccountıd</span><span class="sxs-lookup"><span data-stu-id="09ae8-133">-IntegrationAccountId</span></span>
<span data-ttu-id="09ae8-134">Mantık uygulaması için bir tümleştirme hesap KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-134">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="09ae8-135">-Name</span></span>
<span data-ttu-id="09ae8-136">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-136">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="09ae8-137">-ParameterFilePath</span></span>
<span data-ttu-id="09ae8-138">JSON biçimli parametre dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-138">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-139">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="09ae8-139">-Parameters</span></span>
<span data-ttu-id="09ae8-140">Mantık uygulaması için bir parametre koleksiyonu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="09ae8-141">Karma tablo, sözlük \<string\> veya sözlük belirtin \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="09ae8-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ae8-142">-ResourceGroupName</span></span>
<span data-ttu-id="09ae8-143">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-143">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-144">Durumlu</span><span class="sxs-lookup"><span data-stu-id="09ae8-144">-State</span></span>
<span data-ttu-id="09ae8-145">Mantık uygulamasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="09ae8-146">Bu parametre için kabul edilebilir değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="09ae8-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="09ae8-147">-UseConsumptionModel</span></span>
<span data-ttu-id="09ae8-148">Mantık uygulaması faturaının tüketim tabanlı modeli kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Consumption
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae8-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="09ae8-149">-Confirm</span></span>
<span data-ttu-id="09ae8-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09ae8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ae8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ae8-151">-WhatIf</span></span>
<span data-ttu-id="09ae8-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ae8-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ae8-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09ae8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ae8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ae8-154">CommonParameters</span></span>
<span data-ttu-id="09ae8-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09ae8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ae8-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ae8-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ae8-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09ae8-157">INPUTS</span></span>

### <span data-ttu-id="09ae8-158">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="09ae8-158">None</span></span>
<span data-ttu-id="09ae8-159">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="09ae8-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09ae8-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09ae8-160">OUTPUTS</span></span>

### <span data-ttu-id="09ae8-161">Microsoft. Azure. Management. Logic. modeller. Workflow</span><span class="sxs-lookup"><span data-stu-id="09ae8-161">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="09ae8-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09ae8-162">NOTES</span></span>

## <span data-ttu-id="09ae8-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09ae8-163">RELATED LINKS</span></span>

[<span data-ttu-id="09ae8-164">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="09ae8-164">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="09ae8-165">Yeni-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="09ae8-165">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="09ae8-166">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="09ae8-166">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="09ae8-167">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="09ae8-167">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


