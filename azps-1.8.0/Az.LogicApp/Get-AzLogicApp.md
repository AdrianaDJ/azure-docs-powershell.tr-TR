---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 531a863703ffc0a594f09bade4b9c4044966024a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916084"
---
# <span data-ttu-id="54a4e-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="54a4e-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="54a4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="54a4e-103">Kaynak grubundan bir mantık uygulaması alır.</span><span class="sxs-lookup"><span data-stu-id="54a4e-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="54a4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54a4e-104">SYNTAX</span></span>

### <span data-ttu-id="54a4e-105">Listiş akışları (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54a4e-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54a4e-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="54a4e-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a4e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54a4e-107">DESCRIPTION</span></span>
<span data-ttu-id="54a4e-108">**Get-Azlogicuyg** cmdlet 'i bir mantık uygulaması alır.</span><span class="sxs-lookup"><span data-stu-id="54a4e-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="54a4e-109">Bu cmdlet bir **Iş akışı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="54a4e-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="54a4e-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="54a4e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="54a4e-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="54a4e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="54a4e-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="54a4e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="54a4e-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="54a4e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="54a4e-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54a4e-114">EXAMPLES</span></span>

### <span data-ttu-id="54a4e-115">Örnek 1: kaynak grubundan bir mantık uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="54a4e-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="54a4e-116">Bu komut, ResourceGroup11 adlı kaynak grubundan bir mantık uygulaması alır.</span><span class="sxs-lookup"><span data-stu-id="54a4e-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="54a4e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54a4e-117">PARAMETERS</span></span>

### <span data-ttu-id="54a4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a4e-118">-DefaultProfile</span></span>
<span data-ttu-id="54a4e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="54a4e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54a4e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="54a4e-120">-Name</span></span>
<span data-ttu-id="54a4e-121">Bu cmdlet 'in aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54a4e-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="54a4e-123">Bu cmdlet 'in bir mantık uygulaması aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54a4e-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a4e-124">-Version</span><span class="sxs-lookup"><span data-stu-id="54a4e-124">-Version</span></span>
<span data-ttu-id="54a4e-125">Mantık uygulamasının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="54a4e-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a4e-126">CommonParameters</span></span>
<span data-ttu-id="54a4e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54a4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a4e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a4e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a4e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54a4e-129">INPUTS</span></span>

### <span data-ttu-id="54a4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="54a4e-130">System.String</span></span>

## <span data-ttu-id="54a4e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54a4e-131">OUTPUTS</span></span>

### <span data-ttu-id="54a4e-132">Microsoft. Azure. Management. Logic. modeller. Workflow</span><span class="sxs-lookup"><span data-stu-id="54a4e-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="54a4e-133">Microsoft. Azure. Management. Logic. modeller. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="54a4e-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="54a4e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54a4e-134">NOTES</span></span>

## <span data-ttu-id="54a4e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54a4e-135">RELATED LINKS</span></span>

[<span data-ttu-id="54a4e-136">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="54a4e-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="54a4e-137">Remove-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="54a4e-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="54a4e-138">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="54a4e-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="54a4e-139">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="54a4e-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


