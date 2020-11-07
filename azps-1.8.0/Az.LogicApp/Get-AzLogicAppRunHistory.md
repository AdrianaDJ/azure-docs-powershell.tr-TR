---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: cff5113c37580b375bbaaea24850d5b55cd110ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916075"
---
# <span data-ttu-id="a180d-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a180d-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="a180d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a180d-102">SYNOPSIS</span></span>
<span data-ttu-id="a180d-103">Bir mantık uygulamasının çalışma geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a180d-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="a180d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a180d-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a180d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a180d-105">DESCRIPTION</span></span>
<span data-ttu-id="a180d-106">**Get-AzLogicAppRunHistory** cmdlet 'i, bir mantık uygulamasının çalıştırma geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a180d-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="a180d-107">Bu cmdlet, **Workflowrun** nesneleri koleksiyonunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a180d-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="a180d-108">Mantık uygulamasını ve kaynak grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a180d-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="a180d-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="a180d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a180d-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="a180d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a180d-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="a180d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a180d-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="a180d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a180d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a180d-113">EXAMPLES</span></span>

### <span data-ttu-id="a180d-114">Örnek 1: mantık uygulamasının çalışma geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="a180d-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="a180d-115">Bu komut, LogicApp03 adındaki bir mantık uygulamasının çalışma geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a180d-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="a180d-116">Örnek 2: bir mantık uygulaması çalışması alın</span><span class="sxs-lookup"><span data-stu-id="a180d-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="a180d-117">Bu komut, LogicApp03 adlı mantık uygulaması için belirli bir mantık uygulaması çalıştırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="a180d-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="a180d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a180d-118">PARAMETERS</span></span>

### <span data-ttu-id="a180d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a180d-119">-DefaultProfile</span></span>
<span data-ttu-id="a180d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a180d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a180d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a180d-121">-Name</span></span>
<span data-ttu-id="a180d-122">Bu cmdlet 'in çalışma geçmişi aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a180d-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="a180d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a180d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a180d-124">Mantık uygulamasını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a180d-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="a180d-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="a180d-125">-RunName</span></span>
<span data-ttu-id="a180d-126">Bir mantık uygulamasının çalışma adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a180d-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="a180d-127">Bu cmdlet, bu cmdlet 'in belirttiği iş akışını alır.</span><span class="sxs-lookup"><span data-stu-id="a180d-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="a180d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a180d-128">CommonParameters</span></span>
<span data-ttu-id="a180d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a180d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a180d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a180d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a180d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a180d-131">INPUTS</span></span>

### <span data-ttu-id="a180d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a180d-132">System.String</span></span>

## <span data-ttu-id="a180d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a180d-133">OUTPUTS</span></span>

### <span data-ttu-id="a180d-134">Microsoft. Azure. Management. Logic. modeller. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="a180d-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="a180d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a180d-135">NOTES</span></span>

## <span data-ttu-id="a180d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a180d-136">RELATED LINKS</span></span>

[<span data-ttu-id="a180d-137">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="a180d-137">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="a180d-138">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="a180d-138">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="a180d-139">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a180d-139">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


