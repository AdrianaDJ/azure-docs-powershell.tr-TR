---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: 05ccc9dc237e0058665607488a5083a5295eb2f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764053"
---
# <span data-ttu-id="02d51-101">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="02d51-101">Get-AzureRmLogicAppRunHistory</span></span>

## <span data-ttu-id="02d51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02d51-102">SYNOPSIS</span></span>
<span data-ttu-id="02d51-103">Bir mantık uygulamasının çalışma geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="02d51-103">Gets the run history of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02d51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02d51-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02d51-105">DESCRIPTION</span></span>
<span data-ttu-id="02d51-106">**Get-AzureRmLogicAppRunHistory** cmdlet 'i, bir mantık uygulamasının çalıştırma geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="02d51-106">The **Get-AzureRmLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="02d51-107">Bu cmdlet, **Workflowrun** nesneleri koleksiyonunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="02d51-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="02d51-108">Mantık uygulamasını ve kaynak grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="02d51-108">Specify the logic app and resource group.</span></span>

<span data-ttu-id="02d51-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="02d51-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="02d51-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="02d51-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="02d51-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="02d51-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="02d51-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="02d51-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="02d51-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02d51-113">EXAMPLES</span></span>

### <span data-ttu-id="02d51-114">Örnek 1: mantık uygulamasının çalışma geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="02d51-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="02d51-115">Bu komut, LogicApp03 adındaki bir mantık uygulamasının çalışma geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="02d51-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="02d51-116">Örnek 2: bir mantık uygulaması çalışması alın</span><span class="sxs-lookup"><span data-stu-id="02d51-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="02d51-117">Bu komut, LogicApp03 adlı mantık uygulaması için belirli bir mantık uygulaması çalıştırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="02d51-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="02d51-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02d51-118">PARAMETERS</span></span>

### <span data-ttu-id="02d51-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="02d51-119">-Name</span></span>
<span data-ttu-id="02d51-120">Bu cmdlet 'in çalışma geçmişi aldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02d51-120">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="02d51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d51-121">-ResourceGroupName</span></span>
<span data-ttu-id="02d51-122">Mantık uygulamasını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02d51-122">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="02d51-123">-RunName</span><span class="sxs-lookup"><span data-stu-id="02d51-123">-RunName</span></span>
<span data-ttu-id="02d51-124">Bir mantık uygulamasının çalışma adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02d51-124">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="02d51-125">Bu cmdlet, bu cmdlet 'in belirttiği iş akışını alır.</span><span class="sxs-lookup"><span data-stu-id="02d51-125">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="02d51-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d51-126">-DefaultProfile</span></span>
<span data-ttu-id="02d51-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02d51-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d51-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d51-128">CommonParameters</span></span>
<span data-ttu-id="02d51-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02d51-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d51-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d51-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d51-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02d51-131">INPUTS</span></span>

## <span data-ttu-id="02d51-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02d51-132">OUTPUTS</span></span>

### <span data-ttu-id="02d51-133">Microsoft. Azure. Management. Logic. modeller. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="02d51-133">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="02d51-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02d51-134">NOTES</span></span>

## <span data-ttu-id="02d51-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02d51-135">RELATED LINKS</span></span>

[<span data-ttu-id="02d51-136">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="02d51-136">Get-AzureRmLogicAppRunAction</span></span>](./Get-AzureRmLogicAppRunAction.md)

[<span data-ttu-id="02d51-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="02d51-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

[<span data-ttu-id="02d51-138">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="02d51-138">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


