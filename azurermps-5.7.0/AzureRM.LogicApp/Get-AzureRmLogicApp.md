---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 3faa9ce82806da0e2f058f3d1bcaeba3862c27c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763267"
---
# <span data-ttu-id="59bdf-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="59bdf-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="59bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="59bdf-103">Kaynak grubundan bir mantık uygulaması alır.</span><span class="sxs-lookup"><span data-stu-id="59bdf-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bdf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59bdf-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59bdf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="59bdf-106">**Get-Azurermlogicuygulamacmdlet** 'i bir mantık uygulaması alır.</span><span class="sxs-lookup"><span data-stu-id="59bdf-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="59bdf-107">Bu cmdlet bir **Iş akışı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="59bdf-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="59bdf-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="59bdf-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="59bdf-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="59bdf-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="59bdf-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="59bdf-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="59bdf-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="59bdf-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="59bdf-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59bdf-112">EXAMPLES</span></span>

### <span data-ttu-id="59bdf-113">Örnek 1: kaynak grubundan bir mantık uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="59bdf-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="59bdf-114">Bu komut, ResourceGroup11 adlı kaynak grubundan bir mantık uygulaması alır.</span><span class="sxs-lookup"><span data-stu-id="59bdf-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="59bdf-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59bdf-115">PARAMETERS</span></span>

### <span data-ttu-id="59bdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bdf-116">-DefaultProfile</span></span>
<span data-ttu-id="59bdf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59bdf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59bdf-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="59bdf-118">-Name</span></span>
<span data-ttu-id="59bdf-119">Bu cmdlet 'in aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59bdf-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="59bdf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59bdf-120">-ResourceGroupName</span></span>
<span data-ttu-id="59bdf-121">Bu cmdlet 'in bir mantık uygulaması aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59bdf-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="59bdf-122">-Version</span><span class="sxs-lookup"><span data-stu-id="59bdf-122">-Version</span></span>
<span data-ttu-id="59bdf-123">Mantık uygulamasının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59bdf-123">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="59bdf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bdf-124">CommonParameters</span></span>
<span data-ttu-id="59bdf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59bdf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bdf-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bdf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bdf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59bdf-127">INPUTS</span></span>

### <span data-ttu-id="59bdf-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59bdf-128">None</span></span>
<span data-ttu-id="59bdf-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="59bdf-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59bdf-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59bdf-130">OUTPUTS</span></span>

### <span data-ttu-id="59bdf-131">Microsoft. Azure. Management. Logic. modeller. Workflow</span><span class="sxs-lookup"><span data-stu-id="59bdf-131">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="59bdf-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59bdf-132">NOTES</span></span>

## <span data-ttu-id="59bdf-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59bdf-133">RELATED LINKS</span></span>

[<span data-ttu-id="59bdf-134">Yeni-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="59bdf-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="59bdf-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="59bdf-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="59bdf-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="59bdf-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="59bdf-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="59bdf-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

