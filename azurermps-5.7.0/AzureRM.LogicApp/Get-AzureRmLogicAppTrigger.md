---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: f9f21689a894e46a9cd8d53d591d1cb17099fad8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588202"
---
# <span data-ttu-id="72131-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="72131-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="72131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72131-102">SYNOPSIS</span></span>
<span data-ttu-id="72131-103">Mantık uygulamasının tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="72131-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72131-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72131-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72131-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72131-105">DESCRIPTION</span></span>
<span data-ttu-id="72131-106">**Get-AzureRmLogicAppTrigger** cmdlet 'i bir mantık uygulamasından tetikleri alır.</span><span class="sxs-lookup"><span data-stu-id="72131-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="72131-107">Bu cmdlet bir **Workflowtrigger** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="72131-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="72131-108">İş akışı, kaynak grubu ve tetikleyiciyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="72131-108">Specify the workflow, resource group, and trigger.</span></span>

<span data-ttu-id="72131-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="72131-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="72131-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="72131-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="72131-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="72131-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="72131-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="72131-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="72131-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72131-113">EXAMPLES</span></span>

### <span data-ttu-id="72131-114">Örnek 1: mantık uygulamasının tetikleyicisini alma</span><span class="sxs-lookup"><span data-stu-id="72131-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="72131-115">Bu komut, LogicApp05 adındaki mantık uygulamasından Trigger01 adındaki tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="72131-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="72131-116">Örnek 2: bir mantık uygulamasının tüm tetikleyicilerini alma</span><span class="sxs-lookup"><span data-stu-id="72131-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="72131-117">Bu komut, LogicApp07 adlı mantık uygulamasının tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="72131-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="72131-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72131-118">PARAMETERS</span></span>

### <span data-ttu-id="72131-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72131-119">-DefaultProfile</span></span>
<span data-ttu-id="72131-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72131-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72131-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="72131-121">-Name</span></span>
<span data-ttu-id="72131-122">Bu cmdlet 'in tetik aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72131-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72131-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72131-123">-ResourceGroupName</span></span>
<span data-ttu-id="72131-124">Bu cmdlet 'in tetik aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72131-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="72131-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="72131-125">-TriggerName</span></span>
<span data-ttu-id="72131-126">Bu cmdlet 'in aldığı tetikleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72131-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72131-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72131-127">CommonParameters</span></span>
<span data-ttu-id="72131-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72131-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72131-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72131-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72131-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72131-130">INPUTS</span></span>

### <span data-ttu-id="72131-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="72131-131">None</span></span>
<span data-ttu-id="72131-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="72131-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72131-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72131-133">OUTPUTS</span></span>

### <span data-ttu-id="72131-134">Microsoft. Azure. Management. Logic. modeller. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="72131-134">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="72131-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72131-135">NOTES</span></span>

## <span data-ttu-id="72131-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72131-136">RELATED LINKS</span></span>

[<span data-ttu-id="72131-137">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="72131-137">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="72131-138">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="72131-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


