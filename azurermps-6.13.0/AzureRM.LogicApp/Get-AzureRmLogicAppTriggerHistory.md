---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 9c27fd1e46d17722f843a09babab31338e88e2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764370"
---
# <span data-ttu-id="3cf02-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="3cf02-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="3cf02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf02-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf02-103">Bir mantık uygulamasında tetikleyicilerin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3cf02-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cf02-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cf02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cf02-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf02-106">**Get-AzureRmLogicAppTriggerHistory** cmdlet 'ı, mantık uygulamaları özelliğindeki bir mantık uygulamasında tetikleyicilerin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3cf02-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="3cf02-107">Bu cmdlet bir **Workflowtriggerhistory** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="3cf02-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="3cf02-108">Mantık uygulamasını, kaynak grubunu ve tetikleyiciyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="3cf02-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="3cf02-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="3cf02-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3cf02-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="3cf02-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3cf02-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="3cf02-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3cf02-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="3cf02-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3cf02-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cf02-113">EXAMPLES</span></span>

### <span data-ttu-id="3cf02-114">Örnek 1: mantık uygulamasının tetik geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="3cf02-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="3cf02-115">Bu komut, LogicApp03 adındaki mantık uygulamasında tetik için belirli bir mantık uygulaması tetik geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="3cf02-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="3cf02-116">Örnek 2: bir mantık uygulamasının tetik geçmişlerini alma</span><span class="sxs-lookup"><span data-stu-id="3cf02-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="3cf02-117">Bu komut, LogicApp07 adındaki mantık uygulamasında tetikleyicinin iş akışı tetik geçmişlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3cf02-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="3cf02-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cf02-118">PARAMETERS</span></span>

### <span data-ttu-id="3cf02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf02-119">-DefaultProfile</span></span>
<span data-ttu-id="3cf02-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3cf02-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cf02-121">-Geçmişini adı</span><span class="sxs-lookup"><span data-stu-id="3cf02-121">-HistoryName</span></span>
<span data-ttu-id="3cf02-122">Bu cmdlet 'in aldığı geçmişin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cf02-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3cf02-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cf02-123">-Name</span></span>
<span data-ttu-id="3cf02-124">Bu cmdlet tetik geçmişini aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cf02-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="3cf02-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf02-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cf02-126">Bu cmdlet 'in geçmişi aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cf02-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="3cf02-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="3cf02-127">-TriggerName</span></span>
<span data-ttu-id="3cf02-128">Bu cmdlet 'in geçmişi aldığı tetikleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cf02-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="3cf02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf02-129">CommonParameters</span></span>
<span data-ttu-id="3cf02-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cf02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf02-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf02-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf02-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cf02-132">INPUTS</span></span>

### <span data-ttu-id="3cf02-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf02-133">System.String</span></span>

## <span data-ttu-id="3cf02-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cf02-134">OUTPUTS</span></span>

### <span data-ttu-id="3cf02-135">Microsoft. Azure. Management. Logic. modeller. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="3cf02-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="3cf02-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cf02-136">NOTES</span></span>

## <span data-ttu-id="3cf02-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cf02-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cf02-138">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3cf02-138">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="3cf02-139">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="3cf02-139">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="3cf02-140">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3cf02-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


