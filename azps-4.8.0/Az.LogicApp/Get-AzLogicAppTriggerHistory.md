---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274486"
---
# <span data-ttu-id="cb57f-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="cb57f-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="cb57f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb57f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb57f-103">Bir mantık uygulamasında tetikleyicilerin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="cb57f-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="cb57f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb57f-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb57f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb57f-105">DESCRIPTION</span></span>
<span data-ttu-id="cb57f-106">**Get-AzLogicAppTriggerHistory** cmdlet 'ı, mantık uygulamaları özelliğindeki bir mantık uygulamasında tetikleyicilerin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="cb57f-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="cb57f-107">Bu cmdlet bir **Workflowtriggerhistory** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb57f-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="cb57f-108">Mantık uygulamasını, kaynak grubunu ve tetikleyiciyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="cb57f-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="cb57f-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="cb57f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb57f-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="cb57f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb57f-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="cb57f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb57f-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="cb57f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb57f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb57f-113">EXAMPLES</span></span>

### <span data-ttu-id="cb57f-114">Örnek 1: mantık uygulamasının tetik geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="cb57f-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="cb57f-115">Bu komut, LogicApp03 adındaki mantık uygulamasında tetik için belirli bir mantık uygulaması tetik geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="cb57f-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="cb57f-116">Örnek 2: bir mantık uygulamasının tetik geçmişlerini alma</span><span class="sxs-lookup"><span data-stu-id="cb57f-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="cb57f-117">Bu komut, LogicApp07 adındaki mantık uygulamasında tetikleyicinin iş akışı tetik geçmişlerini alır.</span><span class="sxs-lookup"><span data-stu-id="cb57f-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="cb57f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb57f-118">PARAMETERS</span></span>

### <span data-ttu-id="cb57f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb57f-119">-DefaultProfile</span></span>
<span data-ttu-id="cb57f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cb57f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb57f-121">-Geçmişini adı</span><span class="sxs-lookup"><span data-stu-id="cb57f-121">-HistoryName</span></span>
<span data-ttu-id="cb57f-122">Bu cmdlet 'in aldığı geçmişin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb57f-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cb57f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb57f-123">-Name</span></span>
<span data-ttu-id="cb57f-124">Bu cmdlet tetik geçmişini aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb57f-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="cb57f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb57f-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb57f-126">Bu cmdlet 'in geçmişi aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb57f-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="cb57f-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="cb57f-127">-TriggerName</span></span>
<span data-ttu-id="cb57f-128">Bu cmdlet 'in geçmişi aldığı tetikleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb57f-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="cb57f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb57f-129">CommonParameters</span></span>
<span data-ttu-id="cb57f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb57f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb57f-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb57f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb57f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb57f-132">INPUTS</span></span>

### <span data-ttu-id="cb57f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cb57f-133">System.String</span></span>

## <span data-ttu-id="cb57f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb57f-134">OUTPUTS</span></span>

### <span data-ttu-id="cb57f-135">Microsoft. Azure. Management. Logic. modeller. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="cb57f-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="cb57f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb57f-136">NOTES</span></span>

## <span data-ttu-id="cb57f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb57f-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb57f-138">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="cb57f-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="cb57f-139">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="cb57f-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="cb57f-140">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="cb57f-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


