---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 5b7cc3d2ea0273d0ff96dfca39d4dcb3e169c6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751545"
---
# <span data-ttu-id="e1eb0-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="e1eb0-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="e1eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1eb0-103">Mantık uygulamasının tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="e1eb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1eb0-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1eb0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="e1eb0-106">**Get-AzLogicAppTrigger** cmdlet 'i bir mantık uygulamasından tetikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="e1eb0-107">Bu cmdlet bir **Workflowtrigger** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="e1eb0-108">İş akışı, kaynak grubu ve tetikleyiciyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="e1eb0-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e1eb0-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e1eb0-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e1eb0-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e1eb0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1eb0-113">EXAMPLES</span></span>

### <span data-ttu-id="e1eb0-114">Örnek 1: mantık uygulamasının tetikleyicisini alma</span><span class="sxs-lookup"><span data-stu-id="e1eb0-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="e1eb0-115">Bu komut, LogicApp05 adındaki mantık uygulamasından Trigger01 adındaki tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="e1eb0-116">Örnek 2: bir mantık uygulamasının tüm tetikleyicilerini alma</span><span class="sxs-lookup"><span data-stu-id="e1eb0-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="e1eb0-117">Bu komut, LogicApp07 adlı mantık uygulamasının tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="e1eb0-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1eb0-118">PARAMETERS</span></span>

### <span data-ttu-id="e1eb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1eb0-119">-DefaultProfile</span></span>
<span data-ttu-id="e1eb0-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e1eb0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1eb0-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1eb0-121">-Name</span></span>
<span data-ttu-id="e1eb0-122">Bu cmdlet 'in tetik aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1eb0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1eb0-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1eb0-124">Bu cmdlet 'in tetik aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="e1eb0-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="e1eb0-125">-TriggerName</span></span>
<span data-ttu-id="e1eb0-126">Bu cmdlet 'in aldığı tetikleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1eb0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1eb0-127">CommonParameters</span></span>
<span data-ttu-id="e1eb0-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1eb0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1eb0-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1eb0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1eb0-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1eb0-130">INPUTS</span></span>

### <span data-ttu-id="e1eb0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e1eb0-131">System.String</span></span>

## <span data-ttu-id="e1eb0-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1eb0-132">OUTPUTS</span></span>

### <span data-ttu-id="e1eb0-133">Microsoft. Azure. Management. Logic. modeller. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="e1eb0-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="e1eb0-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1eb0-134">NOTES</span></span>

## <span data-ttu-id="e1eb0-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1eb0-135">RELATED LINKS</span></span>

[<span data-ttu-id="e1eb0-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="e1eb0-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="e1eb0-137">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="e1eb0-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


